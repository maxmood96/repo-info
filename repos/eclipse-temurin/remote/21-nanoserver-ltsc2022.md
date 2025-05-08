## `eclipse-temurin:21-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:e63d13dc49aac2f3a96372e984bbb519769560bf71930f9bbce2c4650b8ce16c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3566; amd64

### `eclipse-temurin:21-nanoserver-ltsc2022` - windows version 10.0.20348.3566; amd64

```console
$ docker pull eclipse-temurin@sha256:095a60e2d80a07398c9fbec0fbcaecbeda36517c509b516d732c0968338c14c8
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.3 MB (324291264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95965b2f6649d209f8ab1415b95ed0b130446aa74ed624edee5bdc83c7bf38b1`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 16 Apr 2025 03:28:26 GMT
RUN Apply image 10.0.20348.3566
# Wed, 23 Apr 2025 17:23:44 GMT
SHELL [cmd /s /c]
# Wed, 23 Apr 2025 17:23:45 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Wed, 23 Apr 2025 17:23:46 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 23 Apr 2025 17:23:48 GMT
USER ContainerAdministrator
# Wed, 23 Apr 2025 17:23:51 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 23 Apr 2025 17:23:52 GMT
USER ContainerUser
# Wed, 23 Apr 2025 17:24:01 GMT
COPY dir:db067bfbcc086396d5dfa4ac3979b5c2114a2c9ec3e102fbc339048e5a829713 in C:\openjdk-21 
# Wed, 23 Apr 2025 17:24:07 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 23 Apr 2025 17:24:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:905464f5b09ec7543cfd4984311153c5e327937892d0e49e145f6b363cf68441`  
		Last Modified: Thu, 08 May 2025 17:04:50 GMT  
		Size: 122.5 MB (122539088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d96dcb76c10988315f8c54fe1b84359309c88293b8ed7d26d0ec728afd87d3`  
		Last Modified: Wed, 23 Apr 2025 17:24:11 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fea4172a77041fc9c83c3a68c1a91948f32c12d0ec8efbea4a01287a8ccd450`  
		Last Modified: Wed, 23 Apr 2025 17:24:11 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5066919245c58ca65100379afb27795d0404e81a0e2cfd010af9071265fdbc8f`  
		Last Modified: Wed, 23 Apr 2025 17:24:11 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8136f51ed3ad019a2ba3a1c05473108b55f7a284970e998ed113b3da2bdbf43f`  
		Last Modified: Wed, 23 Apr 2025 17:24:11 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b71af663050da1a6666c5d178c8f33bcd51e74295389690b7a55109790b39e`  
		Last Modified: Wed, 23 Apr 2025 17:24:10 GMT  
		Size: 76.5 KB (76513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe52caee4028c5daeec5fe91425af6450f9c6b28da1baf474f5b483a8848f143`  
		Last Modified: Wed, 23 Apr 2025 17:24:10 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54455a8307d25aee2e5fde9067d367f7c200ce30681a8ba232c8f5fba82a5f9b`  
		Last Modified: Wed, 23 Apr 2025 17:24:22 GMT  
		Size: 201.6 MB (201551138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2804906c62f4b8b693a59999f51672c1abe42eab10ca90013ff3788f38fe15`  
		Last Modified: Wed, 23 Apr 2025 17:24:10 GMT  
		Size: 118.3 KB (118314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5e8547f8fc1c70af79bf27bba327baffb13cacf1e773e7d5bebc2b0bcfc245`  
		Last Modified: Wed, 23 Apr 2025 17:24:10 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
