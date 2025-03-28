## `openjdk:25-ea-16-nanoserver`

```console
$ docker pull openjdk@sha256:4a1c4839c24eea4fa8c2b289125fc14222da3c18d011498b8c145c5df200adf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3476; amd64
	-	windows version 10.0.20348.3328; amd64
	-	windows version 10.0.17763.7009; amd64

### `openjdk:25-ea-16-nanoserver` - windows version 10.0.26100.3476; amd64

```console
$ docker pull openjdk@sha256:a4556cfd1b93c318494ebba6acce0f8baa6397752c1df53157edf4b2ae22710d
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.4 MB (414402085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39645497e134d10982af22ec85535594606c082424a625d4827f930800dd33c0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Mar 2025 05:48:38 GMT
RUN Apply image 10.0.26100.3476
# Thu, 27 Mar 2025 21:12:51 GMT
SHELL [cmd /s /c]
# Thu, 27 Mar 2025 21:12:52 GMT
ENV JAVA_HOME=C:\openjdk-25
# Thu, 27 Mar 2025 21:12:53 GMT
USER ContainerAdministrator
# Thu, 27 Mar 2025 21:12:56 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Thu, 27 Mar 2025 21:12:56 GMT
USER ContainerUser
# Thu, 27 Mar 2025 21:12:57 GMT
ENV JAVA_VERSION=25-ea+16
# Thu, 27 Mar 2025 21:13:05 GMT
COPY dir:19cd448448f63399f0cc00bb4ac8df0759f681650f72cc2b82002a92d2bbe677 in C:\openjdk-25 
# Thu, 27 Mar 2025 21:13:12 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Thu, 27 Mar 2025 21:13:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6008a43ec9274f69b461027b7f4e2fe6a71387d40072c0b5b4f0dbbfa688d8a5`  
		Last Modified: Wed, 12 Mar 2025 18:43:31 GMT  
		Size: 206.3 MB (206302205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:651258816319f8583025f1126a43a32c925fc488840490f9955160b8db9e2e79`  
		Last Modified: Thu, 27 Mar 2025 21:13:17 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4340e62aef4b69c46cb7da4165a62944688c741bf83adab4765f25b6a0fecbad`  
		Last Modified: Thu, 27 Mar 2025 21:13:17 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec6b6b8caaddefdce854e9694fe716cdcd44c39e79aeb3da62ee3c377fcf6f04`  
		Last Modified: Thu, 27 Mar 2025 21:13:17 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c0f87d2173b3f8dc7aba930e7f55d1caa1ce8b3fd6de40fd97613c22d66940`  
		Last Modified: Thu, 27 Mar 2025 21:13:17 GMT  
		Size: 77.3 KB (77317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:649008fd93c04016d8d6b1126044141dba408beb6d261644066540d42169520f`  
		Last Modified: Thu, 27 Mar 2025 21:13:16 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf5a1e26314899fa0d533da3d3f438da508a4be596be30dd46484b625f65cc3`  
		Last Modified: Thu, 27 Mar 2025 21:13:16 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a89ae1696d95e24c28ddf867966341149fa34d184ac9ac40f70c8b948a6b5ca`  
		Last Modified: Thu, 27 Mar 2025 21:13:27 GMT  
		Size: 207.9 MB (207900707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f04053ea1c19d8b835f4bab6fe6ba001011b2cb44132a37af531c3952f3766b`  
		Last Modified: Thu, 27 Mar 2025 21:13:15 GMT  
		Size: 115.5 KB (115452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7216c98f8d954a9ea74b745ec532e67f77086a87616cda42904bef2317d39b4`  
		Last Modified: Thu, 27 Mar 2025 21:13:15 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-16-nanoserver` - windows version 10.0.20348.3328; amd64

```console
$ docker pull openjdk@sha256:7c55d3cbf90396a31c06af60def58fb09a540a2fd8fc38f5922a1606603b96a1
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.8 MB (328783364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06e61dc1586815eabffc9111207ddbc01f9fc8374a432d48344d97ec3e5b9221`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 06 Mar 2025 10:30:39 GMT
RUN Apply image 10.0.20348.3328
# Thu, 27 Mar 2025 21:00:10 GMT
SHELL [cmd /s /c]
# Thu, 27 Mar 2025 21:00:11 GMT
ENV JAVA_HOME=C:\openjdk-25
# Thu, 27 Mar 2025 21:00:12 GMT
USER ContainerAdministrator
# Thu, 27 Mar 2025 21:00:14 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Thu, 27 Mar 2025 21:00:15 GMT
USER ContainerUser
# Thu, 27 Mar 2025 21:00:15 GMT
ENV JAVA_VERSION=25-ea+16
# Thu, 27 Mar 2025 21:00:23 GMT
COPY dir:19cd448448f63399f0cc00bb4ac8df0759f681650f72cc2b82002a92d2bbe677 in C:\openjdk-25 
# Thu, 27 Mar 2025 21:00:28 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Thu, 27 Mar 2025 21:00:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:47ec0d45ee7716f773dfebb62d84eb3893d3af9baf9c799960566b016a17e330`  
		Last Modified: Wed, 12 Mar 2025 02:22:56 GMT  
		Size: 120.7 MB (120695547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:416c3c0ee530972ee66391f7d7c3ba14967d07dbbcad20f79c6117472c6b4f45`  
		Last Modified: Thu, 27 Mar 2025 21:00:33 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3fb424d3fcdc291cf3a81607d412fd00d3bc48a0e13377727fd1e566d1ed016`  
		Last Modified: Thu, 27 Mar 2025 21:00:33 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d03be61f99d8b8e8afce08290738b2ed785ccb79506ed79e4f3f37e693b5b48`  
		Last Modified: Thu, 27 Mar 2025 21:00:33 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d53526654b591009e11e7d32d5b20b38a33bbf39433ea2e1aced66c2e3f9b81`  
		Last Modified: Thu, 27 Mar 2025 21:00:33 GMT  
		Size: 76.0 KB (76001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54e86ea659cce85531d632375c0f6499a7f4fe613b569a0ed179e01c0817902`  
		Last Modified: Thu, 27 Mar 2025 21:00:32 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f45f637d5382a0b4ddc15efa749e12956f3c3f12a4c54d3f4c3eac412285ef3`  
		Last Modified: Thu, 27 Mar 2025 21:00:32 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41de6ce4c17845621943133737d1d466b7e62e36b560c69f038ac2fa758accab`  
		Last Modified: Thu, 27 Mar 2025 21:00:44 GMT  
		Size: 207.9 MB (207898397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319029c6dfe147da9599a47a6e8604dc4d8f420ac3f6926fc039c527d3e7b479`  
		Last Modified: Thu, 27 Mar 2025 21:00:32 GMT  
		Size: 107.2 KB (107243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b90425a0cb46fbd79277a81d1d68014aa003b331fe5a99694a5e997226a08ff6`  
		Last Modified: Thu, 27 Mar 2025 21:00:32 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-16-nanoserver` - windows version 10.0.17763.7009; amd64

```console
$ docker pull openjdk@sha256:f876170154d52ad898aaebc0d7a667ee24ba1e60d3073dbe01da50facb73410e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.3 MB (319304762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d23a17ebafb62735fd6236dcecc48d12b5740b0c5d67ac8e98022db721a134d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Thu, 27 Mar 2025 21:13:27 GMT
SHELL [cmd /s /c]
# Thu, 27 Mar 2025 21:13:29 GMT
ENV JAVA_HOME=C:\openjdk-25
# Thu, 27 Mar 2025 21:13:29 GMT
USER ContainerAdministrator
# Thu, 27 Mar 2025 21:13:31 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Thu, 27 Mar 2025 21:13:32 GMT
USER ContainerUser
# Thu, 27 Mar 2025 21:13:32 GMT
ENV JAVA_VERSION=25-ea+16
# Thu, 27 Mar 2025 21:13:40 GMT
COPY dir:19cd448448f63399f0cc00bb4ac8df0759f681650f72cc2b82002a92d2bbe677 in C:\openjdk-25 
# Thu, 27 Mar 2025 21:13:45 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Thu, 27 Mar 2025 21:13:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8267004f1f0fc028dab165f507d228139ea336a7126e7fdd4a32d3cd40c3a5`  
		Last Modified: Thu, 27 Mar 2025 21:13:53 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b045c5fbfc0c0c8703b001d0de7e35808a52618cebcb8eae83632f6733ff889`  
		Last Modified: Thu, 27 Mar 2025 21:13:52 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f00d6f09164f9df6b47e9d73f135296d9e439d45f9f77051e55391ee25eed48b`  
		Last Modified: Thu, 27 Mar 2025 21:13:52 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c13c3c62d3e6bad637efd34daeec58629329572b8a94fc84cb14d4860944e511`  
		Last Modified: Thu, 27 Mar 2025 21:13:52 GMT  
		Size: 69.2 KB (69174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2726c956a4676ac3fe218dcfd8f548859b54cd3bfe8df9b6c35b41a84d45547b`  
		Last Modified: Thu, 27 Mar 2025 21:13:50 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5802690e9a3fb7a4b757cd3e7a21b9eb089868580906322ae92de8c9a9d4916`  
		Last Modified: Thu, 27 Mar 2025 21:13:50 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d04fef1de62a23dd9ed7ace5d0e45e3802004ec5d4177a74241a640b2c0569a1`  
		Last Modified: Thu, 27 Mar 2025 21:14:02 GMT  
		Size: 207.9 MB (207899682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f464a7383390ddb6bd81d17fe53be77a418b68ffb2100568610a52d2699f23c`  
		Last Modified: Thu, 27 Mar 2025 21:13:51 GMT  
		Size: 4.4 MB (4421996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e1f36273f92f85b35507d67a19e5f0690bb5b90bb06f777b1955b465980ce04`  
		Last Modified: Thu, 27 Mar 2025 21:13:50 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
