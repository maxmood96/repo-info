## `eclipse-temurin:17-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:324490023e3287e7f4fb3605c5bd3bb2979a1285081c88154dc9db59e832ea87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3207; amd64

### `eclipse-temurin:17-nanoserver-ltsc2022` - windows version 10.0.20348.3207; amd64

```console
$ docker pull eclipse-temurin@sha256:32bc5d3f786f1bfe3d061d66c76a7f0d3abee488d5c2f821351ba49b22e1aee9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.1 MB (308090334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e36f62c6e3d00500d808506be3ffd9fe9d50486903c0932607e5f097b0f3b8cf`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Feb 2025 20:45:43 GMT
RUN Apply image 10.0.20348.3207
# Thu, 13 Feb 2025 01:17:24 GMT
SHELL [cmd /s /c]
# Thu, 13 Feb 2025 01:17:25 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 13 Feb 2025 01:17:25 GMT
ENV JAVA_HOME=C:\openjdk-17
# Thu, 13 Feb 2025 01:17:26 GMT
USER ContainerAdministrator
# Thu, 13 Feb 2025 01:17:28 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 13 Feb 2025 01:17:29 GMT
USER ContainerUser
# Thu, 13 Feb 2025 01:17:36 GMT
COPY dir:5f87ec570fea10148b246e6a91d6cf8396b47b1e19a7e8d79bcea78e84a1d159 in C:\openjdk-17 
# Thu, 13 Feb 2025 01:17:40 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 13 Feb 2025 01:17:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:938e4585b186fc3df3c1959d47ba7a634fea121cec7545db7923ceb191d99a33`  
		Last Modified: Tue, 11 Feb 2025 22:43:09 GMT  
		Size: 120.7 MB (120666610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96a85a1e7c321169232ce970d0099c3936d2e7acd4c38e9dec3239d5b2ed36e8`  
		Last Modified: Thu, 13 Feb 2025 01:17:46 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ff847421f2f707e451b0771bdf7501b02ae34636af830973937afec23981c80`  
		Last Modified: Thu, 13 Feb 2025 01:17:45 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3edf2ad75e774a1fb50fc2f49b220f0f2e0d70ecaf71b9c5ba066b1fc8b9d2f2`  
		Last Modified: Thu, 13 Feb 2025 01:17:45 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8e39c4b8cd83a263e68a80c9ca0e7ffa08a1c45b27e77768e1ec6c9d6f9d5f2`  
		Last Modified: Thu, 13 Feb 2025 01:17:45 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b648ef2af341ec2f76177ed0e419ff809215355474e9f2e5491dccd7aafcd0bd`  
		Last Modified: Thu, 13 Feb 2025 01:17:44 GMT  
		Size: 77.2 KB (77174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb1fae38964c249babe34579ac72c9922bd146b2fd94375d3e56e6a1070573dd`  
		Last Modified: Thu, 13 Feb 2025 01:17:44 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed4241831ba6addc4478f38e4b7941e9948118a9e53877433c1f4fa1f302647`  
		Last Modified: Thu, 13 Feb 2025 01:17:54 GMT  
		Size: 187.2 MB (187233506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a669a941835e2fbf4b1a119a2a9e31ea09d0402fe5ef93937bc42d155914e56e`  
		Last Modified: Thu, 13 Feb 2025 01:17:44 GMT  
		Size: 106.9 KB (106861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:987d3309e6799a87dfff87374968fa1ee5f7ec80151efca741f45c20dbded16c`  
		Last Modified: Thu, 13 Feb 2025 01:17:44 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
