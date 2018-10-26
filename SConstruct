env = Environment(CPPPATH = ['.', 'src'])
src = Glob('src/*.c')
src = src + Glob('cpu/*.S')
env.Library('foslib',src, CFLAGS = ['-g', '-fcolor-diagnostics', '-Werror'], CC = 'clang')
#for uip port
src = Glob('test/test_librws_creation.c')
env.Program('fos',
		src,
		LIBS = ['foslib', 'pthread'],
        	LIBPATH = ['.'], 
        	CCFLAGS = '-DHELLOSCONS',
		CFLAGS = ['-g', '-fcolor-diagnostics', '-fpack-struct',
		'-fno-strict-aliasing', '-Wno-unused-variable', '-Os', '-Wall'],
		CC = 'clang')
