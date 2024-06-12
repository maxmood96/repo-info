## `eclipse-temurin:22-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:83591d954ba6d541cae7aa3bf106a92d4380ee7d991104864107c8cf3d606897
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2527; amd64

### `eclipse-temurin:22-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.2527; amd64

```console
$ docker pull eclipse-temurin@sha256:344250853f8b9c0f4387f774c811d19b64517af94f1548d9ab88ce7fc38fa8cb
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.7 MB (320689198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c6ee38136030be882f06d03dc9fa5c997d32d818225525892af3603b9850645`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jun 2024 08:41:16 GMT
RUN Apply image 10.0.20348.2527
# Wed, 12 Jun 2024 18:27:44 GMT
SHELL [cmd /s /c]
# Wed, 12 Jun 2024 18:33:03 GMT
ENV JAVA_VERSION=jdk-22.0.1+8
# Wed, 12 Jun 2024 18:33:03 GMT
ENV JAVA_HOME=C:\openjdk-22
# Wed, 12 Jun 2024 18:33:04 GMT
USER ContainerAdministrator
# Wed, 12 Jun 2024 18:33:13 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Jun 2024 18:33:14 GMT
USER ContainerUser
# Wed, 12 Jun 2024 18:33:29 GMT
COPY dir:b848142647370c7b57f8798114952350d05bf467cc96eb22cf5219409c8a4580 in C:\openjdk-22 
# Wed, 12 Jun 2024 18:33:43 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 12 Jun 2024 18:33:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f9825bcd6f9509654677a23b5fa1d32b32e1e32ff51914ebfaa76d5e79c22b50`  
		Last Modified: Wed, 12 Jun 2024 02:27:19 GMT  
		Size: 120.5 MB (120488969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ae17666c85b2b00f8e5aa24951a59f0b01a1eb41704faa32e1282e0f0ef217`  
		Last Modified: Wed, 12 Jun 2024 18:52:48 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca9f23647c25d7ffd20f203fcc462773b7d40de69c1bb521a1a311ee563c610`  
		Last Modified: Wed, 12 Jun 2024 18:55:53 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6068732ef9525b4d660e36241562b7663fcc06e9e7541457049db99d6a6bd30`  
		Last Modified: Wed, 12 Jun 2024 18:55:53 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52a68d0423b89de4fa87cb724e47ba677a572ca5bd4fd6ff8d879c0a125b590`  
		Last Modified: Wed, 12 Jun 2024 18:55:53 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5bc581e87d49026aa90c2b0578d55c33da5b05e161cee3750d169e901261b4b`  
		Last Modified: Wed, 12 Jun 2024 18:55:51 GMT  
		Size: 76.3 KB (76333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccc1207aa918c5a176ec3532b5fa6b9fea27428c20c03119c289a4521f6d5bb5`  
		Last Modified: Wed, 12 Jun 2024 18:55:51 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb22d5df619e5c637b75ca6fd2a63c32bc0fc846f482d3e22e6acae2195ab635`  
		Last Modified: Wed, 12 Jun 2024 18:56:10 GMT  
		Size: 200.1 MB (200055718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:705f6ac78c0fff0c08d0bf62468ea10d4b878f9cfd2f9ad11eba38753b5f7ea4`  
		Last Modified: Wed, 12 Jun 2024 18:55:51 GMT  
		Size: 61.2 KB (61218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7314bcbdbe45007b5b5652cc194e45aa89b2b3b05952a43fa833e7da4c4045f4`  
		Last Modified: Wed, 12 Jun 2024 18:55:51 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
