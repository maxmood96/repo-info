## `eclipse-temurin:21-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:f5fa85e542c3190052ed44bb30f613f3616ec93eddf62d242cb8c59a62b0438a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `eclipse-temurin:21-jre-nanoserver-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull eclipse-temurin@sha256:75267bc8d1cda02c946adc6b3394d89302f2d2c1ad72ac5eadbac4f32a916a43
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.3 MB (159310410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30b3b132f32912ebc43fd135f54a366b51512db66bc2e4852e61473138b8478b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Feb 2025 17:59:14 GMT
RUN Apply image 10.0.17763.6893
# Thu, 13 Feb 2025 01:16:42 GMT
SHELL [cmd /s /c]
# Thu, 13 Feb 2025 01:16:43 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Thu, 13 Feb 2025 01:16:44 GMT
ENV JAVA_HOME=C:\openjdk-21
# Thu, 13 Feb 2025 01:16:45 GMT
USER ContainerAdministrator
# Thu, 13 Feb 2025 01:16:47 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 13 Feb 2025 01:16:48 GMT
USER ContainerUser
# Thu, 13 Feb 2025 01:16:52 GMT
COPY dir:c0b7c132c85049081486a93cd76fe016c559b0b921796f63592a768b082ae9e2 in C:\openjdk-21 
# Thu, 13 Feb 2025 01:16:55 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:5965f4f533e4b42b41b3fd8dff42c138329bf35311ce090d4c7cc4acd5a59360`  
		Last Modified: Tue, 11 Feb 2025 20:25:23 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b6355d7ab6026cb57869db6c562b25405168c950299c73228ae3c791c19337f`  
		Last Modified: Thu, 13 Feb 2025 01:16:59 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10d7e85d32b225129ffbf91a1f66b49eb5ca791efeba7c2f48043c417849fa44`  
		Last Modified: Thu, 13 Feb 2025 01:16:59 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb1ff840cbc7f5f8a666999cfb952937f64bd851994ac39b790d816e485a9a0f`  
		Last Modified: Thu, 13 Feb 2025 01:16:59 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4167124fea8946b2d2b1c6dacc4955b74ce2adb907ab23d93ce3d2a8ae5b885`  
		Last Modified: Thu, 13 Feb 2025 01:16:58 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ededf839951e3289cfd26ad494525fec80a3478842975a5b2ad3f32702bce3ba`  
		Last Modified: Thu, 13 Feb 2025 01:16:58 GMT  
		Size: 73.6 KB (73605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3caa1c182d2a0b2e670a32962b58bdf0cecfdf66548e5d1d043df70e1de838d`  
		Last Modified: Thu, 13 Feb 2025 01:16:58 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f84098df1fc6a7b9d02f49fc4b3c3bd2dfeb822d33bd6c5809c0f84c00e965`  
		Last Modified: Thu, 13 Feb 2025 01:17:03 GMT  
		Size: 48.9 MB (48941105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1737ca969ee3a827612511c425618afc74b777b0b9e9826c6d08f82f931e2302`  
		Last Modified: Thu, 13 Feb 2025 01:16:58 GMT  
		Size: 3.4 MB (3375030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
