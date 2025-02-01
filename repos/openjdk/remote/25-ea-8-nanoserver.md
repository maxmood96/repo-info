## `openjdk:25-ea-8-nanoserver`

```console
$ docker pull openjdk@sha256:ccc036f17cbe9925d4d7d2318e17bb1c48753738b3fcee553ccb9a5925527d60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `openjdk:25-ea-8-nanoserver` - windows version 10.0.26100.2894; amd64

```console
$ docker pull openjdk@sha256:6656dc6e800001b1953aafa7725cc06e2fcdfd0eab35cefc9413c1b3e19371eb
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.7 MB (406702263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24d5bfeb80a8324772211fd0d1f66aacbf1a49460df076816a78e92328349abe`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Jan 2025 02:49:59 GMT
RUN Apply image 10.0.26100.2894
# Fri, 31 Jan 2025 23:32:34 GMT
SHELL [cmd /s /c]
# Fri, 31 Jan 2025 23:32:35 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 31 Jan 2025 23:32:36 GMT
USER ContainerAdministrator
# Fri, 31 Jan 2025 23:32:38 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 31 Jan 2025 23:32:39 GMT
USER ContainerUser
# Fri, 31 Jan 2025 23:32:39 GMT
ENV JAVA_VERSION=25-ea+8
# Fri, 31 Jan 2025 23:32:46 GMT
COPY dir:0f89cb81afdb881ec0a835597e0e5b8ef37085da6c3213f99555c2a1da7025d9 in C:\openjdk-25 
# Fri, 31 Jan 2025 23:32:52 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 31 Jan 2025 23:32:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3c572c5b651b10d04181f97ce4c0938b69ad43912e8c0bf19f77a4ea9a8f72e8`  
		Last Modified: Sun, 19 Jan 2025 13:02:58 GMT  
		Size: 199.1 MB (199054258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ddc8dc4bc937d78b80c16900804d5218428251cad8529c8b925da31ff547f7`  
		Last Modified: Fri, 31 Jan 2025 23:32:58 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cfb467b9b6104db3bc8d9ff623f81c48bd6d07c8fc7265d79d31ab81a85d312`  
		Last Modified: Fri, 31 Jan 2025 23:32:57 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6571afb8831e731b2fd3a3ccab200659b4340073e14b82c9392553b488f1ca57`  
		Last Modified: Fri, 31 Jan 2025 23:32:58 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46276aefa9e06d9b69d7e7334b2c0b1c5668067ec4404f03735da26ec851b3e3`  
		Last Modified: Fri, 31 Jan 2025 23:32:58 GMT  
		Size: 76.1 KB (76079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a1e63569cbbdbd0235d13705d273c8fb97d7d1d364521747ba7b7db8fd8a52`  
		Last Modified: Fri, 31 Jan 2025 23:32:56 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcfaf8691b520b201c830140628948f134191da31a46a1e7f96cd938edc35c86`  
		Last Modified: Fri, 31 Jan 2025 23:32:56 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e11830e09d94cedd95fdc1249f8e9e07d99fd8f30942a61ac8fa9b4f4efda7b3`  
		Last Modified: Fri, 31 Jan 2025 23:33:08 GMT  
		Size: 207.5 MB (207472724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fabb2523b460148e2e1fda2cc8aa56acbef4b3f56e68183afd55a377afb82c17`  
		Last Modified: Fri, 31 Jan 2025 23:32:56 GMT  
		Size: 92.9 KB (92912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eda93759bb14b8b21347ff8b80ef4c4c6ec18aa77d926669692c8a74fda22c4`  
		Last Modified: Fri, 31 Jan 2025 23:32:56 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-8-nanoserver` - windows version 10.0.20348.3091; amd64

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

### `openjdk:25-ea-8-nanoserver` - windows version 10.0.17763.6775; amd64

```console
$ docker pull openjdk@sha256:cb02345eafe0170e9bb89ce1a278d3b4c3746a5d06ab77d47dc2c96fd144c71b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.2 MB (367189530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c301ca3c447e4a136837329edb9d00d7f2aa9aae2968b8f65af21289b38eed04`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Fri, 31 Jan 2025 23:28:11 GMT
SHELL [cmd /s /c]
# Fri, 31 Jan 2025 23:28:13 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 31 Jan 2025 23:28:13 GMT
USER ContainerAdministrator
# Fri, 31 Jan 2025 23:28:26 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 31 Jan 2025 23:28:27 GMT
USER ContainerUser
# Fri, 31 Jan 2025 23:28:27 GMT
ENV JAVA_VERSION=25-ea+8
# Fri, 31 Jan 2025 23:28:38 GMT
COPY dir:0f89cb81afdb881ec0a835597e0e5b8ef37085da6c3213f99555c2a1da7025d9 in C:\openjdk-25 
# Fri, 31 Jan 2025 23:28:44 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 31 Jan 2025 23:28:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Tue, 14 Jan 2025 20:45:12 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d42c1ae81224c1ea7ce699b12d192d748b1ecf02e5126df393d7c70b58505a5`  
		Last Modified: Fri, 31 Jan 2025 23:28:50 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ecd80010e5ccd77287110d052a697b5befadb7c54d3bfb1bfddb91340fa299a`  
		Last Modified: Fri, 31 Jan 2025 23:28:49 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959db6ec01878f81bfb9d19996d458d8059d53371d87493c1dc5b14fa15d8889`  
		Last Modified: Fri, 31 Jan 2025 23:28:49 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68cfa1be79b42ef08999307e99bae955cdf605a9b0dab7232763ded67b4c6e11`  
		Last Modified: Fri, 31 Jan 2025 23:28:49 GMT  
		Size: 66.8 KB (66837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde0c8af2b9c7988bb47c659c44c29a2b8b496b27f10b96c19de3286b7eb16b2`  
		Last Modified: Fri, 31 Jan 2025 23:28:48 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b60a5307625f1899dfdfb1b3609a954d54d7a0552c9e0d4ae02106c4c60565`  
		Last Modified: Fri, 31 Jan 2025 23:28:48 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d141b506e164add6a8b2942ce00da282fa8f2895ba6b8fc23981f64f03b8057`  
		Last Modified: Fri, 31 Jan 2025 23:28:59 GMT  
		Size: 207.5 MB (207472832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d5da3c5e36167a92516f9e05d3daa10206d138fcf6e102f0b5031d09e7e5647`  
		Last Modified: Fri, 31 Jan 2025 23:28:48 GMT  
		Size: 4.4 MB (4375962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66cf3f419c9d9ef993600420f9a50b9d26fe704857a0ae32eb990a07f6aa98ad`  
		Last Modified: Fri, 31 Jan 2025 23:28:48 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
