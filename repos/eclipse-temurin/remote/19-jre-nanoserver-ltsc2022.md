## `eclipse-temurin:19-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:00e6b901f8f725f82ee137bcf97851207e99738f7cc91f4bf5d521a7acad8c44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1487; amd64

### `eclipse-temurin:19-jre-nanoserver-ltsc2022` - windows version 10.0.20348.1487; amd64

```console
$ docker pull eclipse-temurin@sha256:46ef520843f86933d0162a93c8138ebe52728a85980c5e57268cbe70fdfa1a7b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.5 MB (167466189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45e8783e954a6e0f359c10a74eeee80ee3d7dba9787644ea5e8f3b9efb1f3238`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Jan 2023 23:36:49 GMT
RUN Apply image 10.0.20348.1487
# Thu, 12 Jan 2023 02:19:48 GMT
SHELL [cmd /s /c]
# Thu, 12 Jan 2023 02:25:35 GMT
ENV JAVA_VERSION=jdk-19.0.1+10
# Thu, 12 Jan 2023 02:25:36 GMT
ENV JAVA_HOME=C:\openjdk-19
# Thu, 12 Jan 2023 02:25:37 GMT
USER ContainerAdministrator
# Thu, 12 Jan 2023 02:25:51 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 12 Jan 2023 02:25:51 GMT
USER ContainerUser
# Thu, 12 Jan 2023 02:26:58 GMT
COPY dir:f8bde2ca36462d5d41624c06c50c3ec39051aaa6a88f0dabf8bb55af828f5608 in C:\openjdk-19 
# Thu, 12 Jan 2023 02:27:15 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:83e9437e818022c1c28f0e07002dd46995c8614e62b9366138fa23b94f43d9ad`  
		Last Modified: Thu, 12 Jan 2023 02:51:06 GMT  
		Size: 122.1 MB (122099566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbebbf572ebe7984b715b8dfe99bc1273403a831c0079b95afa12162b7266f16`  
		Last Modified: Thu, 12 Jan 2023 02:50:38 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fbac7f900a9c01a3fb16d84eedf744987c8045fef7fb7d056174f5136108e77`  
		Last Modified: Thu, 12 Jan 2023 02:53:07 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c16d2606ed201b9849f39a4da4ce8e764ab707f7d6dca05e374564f41672d87`  
		Last Modified: Thu, 12 Jan 2023 02:53:06 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6052e97af270f61fa97aa379410fd26e01069b19613d8fb30e6c13065d61c92e`  
		Last Modified: Thu, 12 Jan 2023 02:53:06 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45075737173e212d3905c32f22add977b909cf031d39042fe28f2b8b8b928181`  
		Last Modified: Thu, 12 Jan 2023 02:53:05 GMT  
		Size: 81.1 KB (81078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e385c57e79b6097f2e28b91a12cdc521c9cb974833d8e9c098e5b03431cd3a38`  
		Last Modified: Thu, 12 Jan 2023 02:53:04 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15f625aa22fb735e8a755558e5db54a1b537a4d8446a3f46e543a308c3840b65`  
		Last Modified: Thu, 12 Jan 2023 02:53:50 GMT  
		Size: 45.2 MB (45219357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7caaeb8a3889e43c3312f64d27dc1237cf4bce08e899236ea3f4a3508b6a04cd`  
		Last Modified: Thu, 12 Jan 2023 02:53:42 GMT  
		Size: 60.9 KB (60856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
