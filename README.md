# AppBundleSample

This project reproduces the issue: https://issuetracker.google.com/issues/117237042

Execute following command,

```
$ ./gradlew bundleDebug --stacktrace
```

then you can see the following error log.

```
* What went wrong:
Execution failed for task ':app:packageDebugBundle'.
> java.util.concurrent.ExecutionException: com.android.tools.build.bundletool.exceptions.BundleFileTypesException$FileUsesReservedNameException: File 'root/AndroidManifest.xml' uses reserved file or directory name 'AndroidManifest.xml'.

* Try:
Run with --info or --debug option to get more log output. Run with --scan to get full insights.

* Exception is:
org.gradle.api.tasks.TaskExecutionException: Execution failed for task ':app:packageDebugBundle'.
        at org.gradle.api.internal.tasks.execution.ExecuteActionsTaskExecuter.executeActions(ExecuteActionsTaskExecuter.java:103)
        at org.gradle.api.internal.tasks.execution.ExecuteActionsTaskExecuter.execute(ExecuteActionsTaskExecuter.java:73)
        at org.gradle.api.internal.tasks.execution.OutputDirectoryCreatingTaskExecuter.execute(OutputDirectoryCreatingTaskExecuter.java:51)
        at org.gradle.api.internal.tasks.execution.SkipUpToDateTaskExecuter.execute(SkipUpToDateTaskExecuter.java:59)
        at org.gradle.api.internal.tasks.execution.ResolveTaskOutputCachingStateExecuter.execute(ResolveTaskOutputCachingStateExecuter.java:54)
        at org.gradle.api.internal.tasks.execution.ValidatingTaskExecuter.execute(ValidatingTaskExecuter.java:59)
        at org.gradle.api.internal.tasks.execution.SkipEmptySourceFilesTaskExecuter.execute(SkipEmptySourceFilesTaskExecuter.java:101)
        at org.gradle.api.internal.tasks.execution.FinalizeInputFilePropertiesTaskExecuter.execute(FinalizeInputFilePropertiesTaskExecuter.java:44)
        at org.gradle.api.internal.tasks.execution.CleanupStaleOutputsExecuter.execute(CleanupStaleOutputsExecuter.java:91)
        at org.gradle.api.internal.tasks.execution.ResolveTaskArtifactStateTaskExecuter.execute(ResolveTaskArtifactStateTaskExecuter.java:62)
        at org.gradle.api.internal.tasks.execution.SkipTaskWithNoActionsExecuter.execute(SkipTaskWithNoActionsExecuter.java:59)
        at org.gradle.api.internal.tasks.execution.SkipOnlyIfTaskExecuter.execute(SkipOnlyIfTaskExecuter.java:54)
        at org.gradle.api.internal.tasks.execution.ExecuteAtMostOnceTaskExecuter.execute(ExecuteAtMostOnceTaskExecuter.java:43)
        at org.gradle.api.internal.tasks.execution.CatchExceptionTaskExecuter.execute(CatchExceptionTaskExecuter.java:34)
        at org.gradle.execution.taskgraph.DefaultTaskGraphExecuter$EventFiringTaskWorker$1.run(DefaultTaskGraphExecuter.java:256)
        at org.gradle.internal.progress.DefaultBuildOperationExecutor$RunnableBuildOperationWorker.execute(DefaultBuildOperationExecutor.java:336)
        at org.gradle.internal.progress.DefaultBuildOperationExecutor$RunnableBuildOperationWorker.execute(DefaultBuildOperationExecutor.java:328)
        at org.gradle.internal.progress.DefaultBuildOperationExecutor.execute(DefaultBuildOperationExecutor.java:199)
        at org.gradle.internal.progress.DefaultBuildOperationExecutor.run(DefaultBuildOperationExecutor.java:110)
        at org.gradle.execution.taskgraph.DefaultTaskGraphExecuter$EventFiringTaskWorker.execute(DefaultTaskGraphExecuter.java:249)
        at org.gradle.execution.taskgraph.DefaultTaskGraphExecuter$EventFiringTaskWorker.execute(DefaultTaskGraphExecuter.java:238)
        at org.gradle.execution.taskgraph.DefaultTaskPlanExecutor$TaskExecutorWorker.processTask(DefaultTaskPlanExecutor.java:123)
        at org.gradle.execution.taskgraph.DefaultTaskPlanExecutor$TaskExecutorWorker.access$200(DefaultTaskPlanExecutor.java:79)
        at org.gradle.execution.taskgraph.DefaultTaskPlanExecutor$TaskExecutorWorker$1.execute(DefaultTaskPlanExecutor.java:104)
        at org.gradle.execution.taskgraph.DefaultTaskPlanExecutor$TaskExecutorWorker$1.execute(DefaultTaskPlanExecutor.java:98)
        at org.gradle.execution.taskgraph.DefaultTaskExecutionPlan.execute(DefaultTaskExecutionPlan.java:663)
        at org.gradle.execution.taskgraph.DefaultTaskExecutionPlan.executeWithTask(DefaultTaskExecutionPlan.java:597)
        at org.gradle.execution.taskgraph.DefaultTaskPlanExecutor$TaskExecutorWorker.run(DefaultTaskPlanExecutor.java:98)
        at org.gradle.internal.concurrent.ExecutorPolicy$CatchAndRecordFailures.onExecute(ExecutorPolicy.java:63)
        at org.gradle.internal.concurrent.ManagedExecutorImpl$1.run(ManagedExecutorImpl.java:46)
        at org.gradle.internal.concurrent.ThreadFactoryImpl$ManagedThreadRunnable.run(ThreadFactoryImpl.java:55)
Caused by: org.gradle.internal.UncheckedException: java.util.concurrent.ExecutionException: com.android.tools.build.bundletool.exceptions.BundleFileTypesException$FileUsesReservedNameException: File 'root/AndroidManifest.xml' uses reserved file or directory name 'AndroidManifest.xml'.
        at org.gradle.internal.UncheckedException.throwAsUncheckedException(UncheckedException.java:63)
        at org.gradle.internal.UncheckedException.throwAsUncheckedException(UncheckedException.java:40)
        at org.gradle.internal.reflect.JavaMethod.invoke(JavaMethod.java:76)
        at org.gradle.api.internal.project.taskfactory.StandardTaskAction.doExecute(StandardTaskAction.java:46)
        at org.gradle.api.internal.project.taskfactory.StandardTaskAction.execute(StandardTaskAction.java:39)
        at org.gradle.api.internal.project.taskfactory.StandardTaskAction.execute(StandardTaskAction.java:26)
        at org.gradle.api.internal.AbstractTask$TaskActionWrapper.execute(AbstractTask.java:788)
        at org.gradle.api.internal.AbstractTask$TaskActionWrapper.execute(AbstractTask.java:755)
        at org.gradle.api.internal.tasks.execution.ExecuteActionsTaskExecuter$1.run(ExecuteActionsTaskExecuter.java:124)
        at org.gradle.internal.progress.DefaultBuildOperationExecutor$RunnableBuildOperationWorker.execute(DefaultBuildOperationExecutor.java:336)
        at org.gradle.internal.progress.DefaultBuildOperationExecutor$RunnableBuildOperationWorker.execute(DefaultBuildOperationExecutor.java:328)
        at org.gradle.internal.progress.DefaultBuildOperationExecutor.execute(DefaultBuildOperationExecutor.java:199)
        at org.gradle.internal.progress.DefaultBuildOperationExecutor.run(DefaultBuildOperationExecutor.java:110)
        at org.gradle.api.internal.tasks.execution.ExecuteActionsTaskExecuter.executeAction(ExecuteActionsTaskExecuter.java:113)
        at org.gradle.api.internal.tasks.execution.ExecuteActionsTaskExecuter.executeActions(ExecuteActionsTaskExecuter.java:95)
        ... 30 more
Caused by: java.util.concurrent.ExecutionException: com.android.tools.build.bundletool.exceptions.BundleFileTypesException$FileUsesReservedNameException: File 'root/AndroidManifest.xml' uses reserved file or directory name 'AndroidManifest.xml'.
        at com.android.ide.common.workers.ExecutorServiceAdapter.close(ExecutorServiceAdapter.kt:56)
        at kotlin.io.CloseableKt.closeFinally(Closeable.kt:65)
        at com.android.build.gradle.internal.tasks.BundleTask.bundleModules(BundleTask.kt:128)
        at org.gradle.internal.reflect.JavaMethod.invoke(JavaMethod.java:73)
        ... 42 more
Caused by: com.android.tools.build.bundletool.exceptions.BundleFileTypesException$FileUsesReservedNameException: File 'root/AndroidManifest.xml' uses reserved file or directory name 'AndroidManifest.xml'.
        at com.android.tools.build.bundletool.validation.BundleFilesValidator.validateModuleFile(BundleFilesValidator.java:112)
        at com.android.tools.build.bundletool.validation.ValidatorRunner.validateBundleModulesUsingSubValidator(ValidatorRunner.java:81)
        at com.android.tools.build.bundletool.validation.ValidatorRunner.lambda$validateBundleModules$4(ValidatorRunner.java:64)
        at com.google.common.collect.ImmutableList.forEach(ImmutableList.java:406)
        at com.android.tools.build.bundletool.validation.ValidatorRunner.validateBundleModules(ValidatorRunner.java:63)
        at com.android.tools.build.bundletool.validation.BundleModulesValidator.validate(BundleModulesValidator.java:101)
        at com.android.tools.build.bundletool.commands.BuildBundleCommand.validateInput(BuildBundleCommand.java:244)
        at com.android.tools.build.bundletool.commands.BuildBundleCommand.execute(BuildBundleCommand.java:162)
        at com.android.build.gradle.internal.tasks.BundleTask$BundleToolRunnable.run(BundleTask.kt:201)
        at com.android.ide.common.workers.ExecutorServiceAdapter$submit$submission$1.run(ExecutorServiceAdapter.kt:39)
        ... 46 more
```