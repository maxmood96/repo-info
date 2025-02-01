## `openjdk:25-ea-8-jdk-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:d384d171469c3675c7ee9ee508e13fd5329b7a316a19a320251a5c54a6a31e1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `openjdk:25-ea-8-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull openjdk@sha256:11fa283735f3cd18bb225ec2c02d9db86147cd622355aed82a10fcf39cda75c2
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.3 MB (328311283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f110b0c4ec4efc6327ba768aaaf3366db917727e16233d5582606438f197cf3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 12 Jan 2025 09:54:50 GMT
RUN Apply image 10.0.20348.3091
# Fri, 31 Jan 2025 23:27:45 GMT
SHELL [cmd /s /c]
# Fri, 31 Jan 2025 23:27:46 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 31 Jan 2025 23:27:46 GMT
USER ContainerAdministrator
# Fri, 31 Jan 2025 23:27:51 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 31 Jan 2025 23:27:52 GMT
USER ContainerUser
# Fri, 31 Jan 2025 23:27:52 GMT
ENV JAVA_VERSION=25-ea+8
# Fri, 31 Jan 2025 23:27:59 GMT
COPY dir:0f89cb81afdb881ec0a835597e0e5b8ef37085da6c3213f99555c2a1da7025d9 in C:\openjdk-25 
# Fri, 31 Jan 2025 23:28:04 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 31 Jan 2025 23:28:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fd3058b29fbd287119a2fa4d2d36a46fdee3bbada5fd9ef6f02f2d7d4cc143ab`  
		Last Modified: Tue, 14 Jan 2025 20:27:35 GMT  
		Size: 120.7 MB (120661554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f94dbaa3427d9892f340368e1b3c83190a9979b87b9fc393ead894dafa17d1fd`  
		Last Modified: Fri, 31 Jan 2025 23:28:11 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7287793b632822da2627c7ff7122d4ec92f990315dc688ba018665937c3c6ed`  
		Last Modified: Fri, 31 Jan 2025 23:28:11 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd5e7eddbba04c8e8376c09e45fc267e072148f4fafa02c8d10c1dab82883fbf`  
		Last Modified: Fri, 31 Jan 2025 23:28:11 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40aaf63dbe23b9ec7b00c77617bfce1d4a450f59974e1248372e302bf9fe88c`  
		Last Modified: Fri, 31 Jan 2025 23:28:11 GMT  
		Size: 74.0 KB (74038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f4faeee20fb431917a5ff6c3fbc17bf4b5852135f41209d7a6e567960dffc7`  
		Last Modified: Fri, 31 Jan 2025 23:28:09 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:228ba934e68c5980e3bfc92e90459cf0862f5485712ba3db9c2a9ae199c2454c`  
		Last Modified: Fri, 31 Jan 2025 23:28:09 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6753afe5957bbe0f4a49e50ec74f92824f1edc0df1b111c2f4dc32f4e7dcdb74`  
		Last Modified: Fri, 31 Jan 2025 23:28:20 GMT  
		Size: 207.5 MB (207471734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:152fabe95dc2819a4cae8454c55f7ac99571bab4a58c266f11290821bfb83d8a`  
		Last Modified: Fri, 31 Jan 2025 23:28:09 GMT  
		Size: 97.7 KB (97730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc42f4a4049ef879ead2e6c7771eb3187318a825609d7570fd165391f45381e3`  
		Last Modified: Fri, 31 Jan 2025 23:28:09 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
