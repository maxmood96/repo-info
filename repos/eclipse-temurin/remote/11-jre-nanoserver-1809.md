## `eclipse-temurin:11-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:9ca47d83a028e4266b2cd6aba151a1f4e6317347226127d4618fd1365bdb7367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `eclipse-temurin:11-jre-nanoserver-1809` - windows version 10.0.17763.6054; amd64

```console
$ docker pull eclipse-temurin@sha256:b5a8439ec9a27e7b013e5fd66bbe88560f348b136ad302d392fb630468a8b20f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.5 MB (198513070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a46c35bb5e74efc2cccb7da8da9b07cf373bddf85a84f1373f9f833447553eec`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 03 Jul 2024 00:02:58 GMT
RUN Apply image 10.0.17763.6054
# Wed, 10 Jul 2024 16:38:43 GMT
SHELL [cmd /s /c]
# Wed, 24 Jul 2024 01:21:01 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Wed, 24 Jul 2024 01:21:01 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 24 Jul 2024 01:21:02 GMT
USER ContainerAdministrator
# Wed, 24 Jul 2024 01:21:13 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 24 Jul 2024 01:21:14 GMT
USER ContainerUser
# Wed, 24 Jul 2024 01:25:43 GMT
COPY dir:d312cd25f7717f1c23a729ceda7f0a5b69cc56184795f5759819b3fb155af4e0 in C:\openjdk-11 
# Wed, 24 Jul 2024 01:25:53 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:53308e1345e8a502fe824770c132f9d645d42108fee87a0708ea8814c901e40d`  
		Last Modified: Tue, 09 Jul 2024 17:42:24 GMT  
		Size: 155.1 MB (155081383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c00a79547db1bc3ab4a5550f2ec9ba165e302f4a4984af3c1bfbbbe1726a3bf6`  
		Last Modified: Wed, 10 Jul 2024 17:28:00 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa488de0e4d919f5a414618d07d781e2cdcad9a0d533c1c519faa4505ccffe7`  
		Last Modified: Wed, 24 Jul 2024 02:23:10 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fe226e31ec8082ba27b93d6437d91e61a55584eeea4841839c8062ad4c90090`  
		Last Modified: Wed, 24 Jul 2024 02:23:10 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d70a48df53bfc58e073ca92be0cb9907843eda0cf4920229e005922f36eda3b5`  
		Last Modified: Wed, 24 Jul 2024 02:23:09 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2935327bfad2d8994fee4429feedc3b9f95fbfb085cb02d8b5da6bc10228ed15`  
		Last Modified: Wed, 24 Jul 2024 02:23:08 GMT  
		Size: 75.4 KB (75390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8cc6b4cc5f9bb1deac3a6fd56c4d9aad5fd461f05f5456e2df4688b846932a6`  
		Last Modified: Wed, 24 Jul 2024 02:23:07 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23458d534ba442b7e4d14750660a2cbdc4c4aee0236770ea64c3251c93a76429`  
		Last Modified: Wed, 24 Jul 2024 02:24:18 GMT  
		Size: 43.3 MB (43263077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18c18ceba4a37d9569f10faaf37350bda68a74f3194a5ed0be1de32f10e436d`  
		Last Modified: Wed, 24 Jul 2024 02:24:10 GMT  
		Size: 87.5 KB (87496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
