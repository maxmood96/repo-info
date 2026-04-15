## `eclipse-temurin:26_35-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:2391f2539a2732cc24993f422756bd1f3cfd4a4683b91d9f2538004b359d8f81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `eclipse-temurin:26_35-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull eclipse-temurin@sha256:2bb019aeaebb7369d4714d6d8d0ec4f961c058707a15df7c8aa19611c44a3ff2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.5 MB (268461304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe5890653c4cb719b8fc2d19b7a94dcbb4a0f0f09294714a826006e69b68850`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Tue, 14 Apr 2026 22:10:49 GMT
SHELL [cmd /s /c]
# Tue, 14 Apr 2026 22:12:24 GMT
ENV JAVA_VERSION=jdk-26+35
# Tue, 14 Apr 2026 22:12:25 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 14 Apr 2026 22:12:25 GMT
USER ContainerAdministrator
# Tue, 14 Apr 2026 22:12:27 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 14 Apr 2026 22:12:27 GMT
USER ContainerUser
# Tue, 14 Apr 2026 22:12:34 GMT
COPY dir:8f93d89558d485d03b81034182d43f2557754598b0731c760b32ca0af365b3c1 in C:\openjdk-26 
# Tue, 14 Apr 2026 22:12:39 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 14 Apr 2026 22:12:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f577f04bf25fbe8b679de7ed1a1bb3aec05c54b5f22de311414b5b7e7dbe8fb5`  
		Last Modified: Tue, 14 Apr 2026 22:11:03 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a04590e8f5cce512e8fc4cb4afec0256bd48facbf58f671acc14e7526f58d0a5`  
		Last Modified: Tue, 14 Apr 2026 22:12:45 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a395cd3b71e7726a51fd752488bffbf071e5437ef084235af32faf7751c1ac0`  
		Last Modified: Tue, 14 Apr 2026 22:12:45 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57183c9776244ce58d20f688a8d436ffaf3d5fb1a52359f284c41aebcaeb564f`  
		Last Modified: Tue, 14 Apr 2026 22:12:45 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82c083f2e8acb8155ec22380fe50bb24c2f41737a79fa273fcda8713fd21a7a1`  
		Last Modified: Tue, 14 Apr 2026 22:12:43 GMT  
		Size: 74.5 KB (74457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce4c7eaea93f3ccf3a62253419e86302561d5a501aea89ad708274f64d2f0f81`  
		Last Modified: Tue, 14 Apr 2026 22:12:43 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7be27d758035bc18b9ab6eadb04860ffa38a0560efba522735c21984da6b4cd`  
		Last Modified: Tue, 14 Apr 2026 22:12:56 GMT  
		Size: 141.3 MB (141306830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df603b9ecec9b7b91283d804cbcd7fb614c37e35887e6606a7aa5b6c5cf7d528`  
		Last Modified: Tue, 14 Apr 2026 22:12:43 GMT  
		Size: 117.7 KB (117714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c6b7efb07e1a6f5d571eb641fed19caed29d92d3527675aa9e27484812a82f`  
		Last Modified: Tue, 14 Apr 2026 22:12:43 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
