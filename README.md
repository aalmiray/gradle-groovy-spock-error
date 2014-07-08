
------------------------------------------------------------
Gradle 2.0
------------------------------------------------------------

Build time:   2014-07-01 07:45:34 UTC

Build number: none

Revision:     b6ead6fa452dfdadec484059191eb641d817226c

Groovy:       2.3.3

Ant:          Apache Ant(TM) version 1.9.3 compiled on December 23 2013

JVM:          1.7.0_60 (Oracle Corporation 24.60-b09)

OS:           Mac OS X 10.9.3 x86_64



Spock yields the following error

    org.spockframework.util.InternalSpockError: Failed to instantiate spec 'FooSpec'
        at org.spockframework.runtime.BaseSpecRunner.createSpecInstance(BaseSpecRunner.java:130)
        at org.spockframework.runtime.BaseSpecRunner.run(BaseSpecRunner.java:80)
        at org.spockframework.runtime.Sputnik.run(Sputnik.java:63)
        at org.gradle.api.internal.tasks.testing.junit.JUnitTestClassExecuter.runTestClass(JUnitTestClassExecuter.java:86)
        at org.gradle.api.internal.tasks.testing.junit.JUnitTestClassExecuter.execute(JUnitTestClassExecuter.java:49)
        at org.gradle.api.internal.tasks.testing.junit.JUnitTestClassProcessor.processTestClass(JUnitTestClassProcessor.java:69)
        at org.gradle.api.internal.tasks.testing.SuiteTestClassProcessor.processTestClass(SuiteTestClassProcessor.java:48)
        at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
        at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:57)
        at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
        at java.lang.reflect.Method.invoke(Method.java:606)
        at org.gradle.messaging.dispatch.ReflectionDispatch.dispatch(ReflectionDispatch.java:35)
        at org.gradle.messaging.dispatch.ReflectionDispatch.dispatch(ReflectionDispatch.java:24)
        at org.gradle.messaging.dispatch.ContextClassLoaderDispatch.dispatch(ContextClassLoaderDispatch.java:32)
        at org.gradle.messaging.dispatch.ProxyDispatchAdapter$DispatchingInvocationHandler.invoke(ProxyDispatchAdapter.java:93)
        at com.sun.proxy.$Proxy2.processTestClass(Unknown Source)
        at org.gradle.api.internal.tasks.testing.worker.TestWorker.processTestClass(TestWorker.java:105)
        at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
        at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:57)
        at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
        at java.lang.reflect.Method.invoke(Method.java:606)
        at org.gradle.messaging.dispatch.ReflectionDispatch.dispatch(ReflectionDispatch.java:35)
        at org.gradle.messaging.dispatch.ReflectionDispatch.dispatch(ReflectionDispatch.java:24)
        at org.gradle.messaging.remote.internal.hub.MessageHub$Handler.run(MessageHub.java:355)
        at org.gradle.internal.concurrent.DefaultExecutorFactory$StoppableExecutorImpl$1.run(DefaultExecutorFactory.java:64)
        at java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1145)
        at java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:615)
        at java.lang.Thread.run(Thread.java:745)
    Caused by: java.lang.ExceptionInInitializerError
        at org.codehaus.groovy.reflection.ClassInfo.isValidWeakMetaClass(ClassInfo.java:221)
        at org.codehaus.groovy.reflection.ClassInfo.getMetaClassForClass(ClassInfo.java:191)
        at org.codehaus.groovy.reflection.ClassInfo.getMetaClass(ClassInfo.java:236)
        at sample.FooSpec.$getStaticMetaClass(FooSpec.groovy)
        at sample.FooSpec.<init>(FooSpec.groovy)
        at sun.reflect.NativeConstructorAccessorImpl.newInstance0(Native Method)
        at sun.reflect.NativeConstructorAccessorImpl.newInstance(NativeConstructorAccessorImpl.java:57)
        at sun.reflect.DelegatingConstructorAccessorImpl.newInstance(DelegatingConstructorAccessorImpl.java:45)
        at java.lang.reflect.Constructor.newInstance(Constructor.java:526)
        at java.lang.Class.newInstance(Class.java:374)
        at org.spockframework.runtime.BaseSpecRunner.createSpecInstance(BaseSpecRunner.java:121)
        ... 27 more
    Caused by: groovy.lang.GroovyRuntimeException: Conflicting module versions. Module [groovy-all is loaded in version 2.3.3 and you are trying to load version 2.3.4
        at org.codehaus.groovy.runtime.metaclass.MetaClassRegistryImpl$DefaultModuleListener.onModule(MetaClassRegistryImpl.java:509)
        at org.codehaus.groovy.runtime.m12n.ExtensionModuleScanner.scanExtensionModuleFromProperties(ExtensionModuleScanner.java:78)
        at org.codehaus.groovy.runtime.m12n.ExtensionModuleScanner.scanExtensionModuleFromMetaInf(ExtensionModuleScanner.java:72)
        at org.codehaus.groovy.runtime.m12n.ExtensionModuleScanner.scanClasspathModules(ExtensionModuleScanner.java:54)
        at org.codehaus.groovy.runtime.metaclass.MetaClassRegistryImpl.<init>(MetaClassRegistryImpl.java:110)
        at org.codehaus.groovy.runtime.metaclass.MetaClassRegistryImpl.<init>(MetaClassRegistryImpl.java:71)
        at groovy.lang.GroovySystem.<clinit>(GroovySystem.java:33)
        ... 38 more


