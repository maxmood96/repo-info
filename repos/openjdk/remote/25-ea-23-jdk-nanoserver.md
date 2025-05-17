## `openjdk:25-ea-23-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:e0e02e8fd3628789b27bbe802c1ff6aa5916708fd59f2c825e509e4220466bd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.4061; amd64
	-	windows version 10.0.20348.3692; amd64
	-	windows version 10.0.17763.7314; amd64

### `openjdk:25-ea-23-jdk-nanoserver` - windows version 10.0.26100.4061; amd64

```console
$ docker pull openjdk@sha256:6ace5329eb455c537fb0cb980d51d0d78bb8cea4f11bee1f987a0c6d91733b26
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.5 MB (400529300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804971ff413d602ca8f0e1605e011c2e54a67bcb61329690b09b3828096f2f5e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 10 May 2025 00:58:48 GMT
RUN Apply image 10.0.26100.4061
# Fri, 16 May 2025 21:13:37 GMT
SHELL [cmd /s /c]
# Fri, 16 May 2025 21:13:38 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 16 May 2025 21:13:39 GMT
USER ContainerAdministrator
# Fri, 16 May 2025 21:13:42 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 16 May 2025 21:13:42 GMT
USER ContainerUser
# Fri, 16 May 2025 21:13:43 GMT
ENV JAVA_VERSION=25-ea+23
# Fri, 16 May 2025 21:13:51 GMT
COPY dir:be99341787be1c3f0d565e6ac1d9202629ef201376adf519d795dfb5baaa83fe in C:\openjdk-25 
# Fri, 16 May 2025 21:13:58 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 16 May 2025 21:13:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9824510349be04d2eb26f9aaba1d016eddcbed10bdcd6681f4636c948766f3d1`  
		Last Modified: Thu, 15 May 2025 20:15:30 GMT  
		Size: 191.4 MB (191412015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ee97e4a225f190885c8aa2b7943f296eb6abd10a185ea32a7043b0d4754e90`  
		Last Modified: Fri, 16 May 2025 21:14:46 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b00dcdbb90acf4badb49ebbfa692589ecddab522108848b6ba2b6fe6bd8bbc`  
		Last Modified: Fri, 16 May 2025 21:14:46 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edb43016baaf3ae4792eb1133d66a4293c9d74b406d79510bf2e3499a0c710eb`  
		Last Modified: Fri, 16 May 2025 21:14:46 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39c13378b2ddc602b53e6227e369089729278ee49599e19f369e360b5417743`  
		Last Modified: Fri, 16 May 2025 21:14:46 GMT  
		Size: 76.6 KB (76584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2d878af9a1d89335e50590663ea6ff95019d70da97af215b502a2d7e48caf8`  
		Last Modified: Fri, 16 May 2025 21:14:47 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ad6ed16b3f1c1fbda893bcbacd224a0aa46fb28fe2b5dba9483be566ed074f`  
		Last Modified: Fri, 16 May 2025 21:14:48 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a82fb2c7d125ea893de1cbc897b38577a4039d6c265bd744ede8ad5d9ff2224`  
		Last Modified: Sat, 17 May 2025 00:23:56 GMT  
		Size: 208.9 MB (208919878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feaa4455312e51dfdd23927dac9994417af6b3d63b7ea84d52f6d018e85427ac`  
		Last Modified: Fri, 16 May 2025 21:14:48 GMT  
		Size: 114.5 KB (114494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41933a6ec070fb5ded6fed14447860ea41ed5d54b3fa2ee95dadc7b33fd2cc78`  
		Last Modified: Fri, 16 May 2025 21:14:48 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-23-jdk-nanoserver` - windows version 10.0.20348.3692; amd64

```console
$ docker pull openjdk@sha256:dc927bbc6cbe29661fe2892c22969453d2af5d1997cbbe08ab60504154c9fbac
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.7 MB (331682287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5cbd628d27984fe41d8646e56b275fcf4f77de677aa881df4d630fd37209960`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 09 May 2025 19:22:57 GMT
RUN Apply image 10.0.20348.3692
# Fri, 16 May 2025 21:11:45 GMT
SHELL [cmd /s /c]
# Fri, 16 May 2025 21:11:46 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 16 May 2025 21:11:46 GMT
USER ContainerAdministrator
# Fri, 16 May 2025 21:11:48 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 16 May 2025 21:11:49 GMT
USER ContainerUser
# Fri, 16 May 2025 21:11:49 GMT
ENV JAVA_VERSION=25-ea+23
# Fri, 16 May 2025 21:11:57 GMT
COPY dir:be99341787be1c3f0d565e6ac1d9202629ef201376adf519d795dfb5baaa83fe in C:\openjdk-25 
# Fri, 16 May 2025 21:12:02 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 16 May 2025 21:12:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:46eb56853bf7d519201d6623d174cec4d04bea0e9d1426f76cc99e437f341f3a`  
		Last Modified: Thu, 15 May 2025 19:27:55 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3adbe9ed8706c1c699d1ca44b8411effc72d88e948840b6a1211f4e007cc5b95`  
		Last Modified: Fri, 16 May 2025 21:12:44 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889bb7ed8caac1ecc5809484a9d82082cd5823575c13429fad97e87488484947`  
		Last Modified: Fri, 16 May 2025 21:12:45 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ed751f159ba3c09fffb9cc49e66ce46e2f14b4d9dcfa0d19b12b7d52627fc13`  
		Last Modified: Fri, 16 May 2025 21:12:45 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:024cb9d3e7b662f33cf7a51ae4987db0f8b5f2e45188ba289c16ff53ee29a71a`  
		Last Modified: Fri, 16 May 2025 21:12:45 GMT  
		Size: 76.5 KB (76470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae10ccfeb81cbfe8491ed7f40d9d9e019a9e520efe9cfb073d0398f76d7b187d`  
		Last Modified: Fri, 16 May 2025 21:12:45 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dca2042cc5a5f000130e062ccb965ed20a01c0ca8f6a0f6df04f8502b5631a8`  
		Last Modified: Fri, 16 May 2025 21:12:45 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ed4226f120febb09227d11b848f25646fb3d1424823804c5970d4d6dcedba93`  
		Last Modified: Sat, 17 May 2025 00:24:03 GMT  
		Size: 208.9 MB (208915406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41366ce39d24109a6f497442bfae6809c344d1d61e77dce5cbb061c389f71666`  
		Last Modified: Fri, 16 May 2025 21:12:45 GMT  
		Size: 107.6 KB (107591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe232b14acad8d95efee54346dbaeffa8976ba7c37b504c0b1f648d6f1972a8a`  
		Last Modified: Fri, 16 May 2025 21:12:46 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-23-jdk-nanoserver` - windows version 10.0.17763.7314; amd64

```console
$ docker pull openjdk@sha256:bdcd5c81b51b25a86de94e953a21d7a1a4ab09b3ac257d1e6e260a7eb8acafec
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.2 MB (322213408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b56dc9c074f346f456b4b26d3cd2a34f2c6be9b81e2be4fac14cb5ba96106cfa`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 09 May 2025 13:34:54 GMT
RUN Apply image 10.0.17763.7314
# Fri, 16 May 2025 21:13:04 GMT
SHELL [cmd /s /c]
# Fri, 16 May 2025 21:13:05 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 16 May 2025 21:13:05 GMT
USER ContainerAdministrator
# Fri, 16 May 2025 21:13:08 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 16 May 2025 21:13:08 GMT
USER ContainerUser
# Fri, 16 May 2025 21:13:09 GMT
ENV JAVA_VERSION=25-ea+23
# Fri, 16 May 2025 21:13:18 GMT
COPY dir:be99341787be1c3f0d565e6ac1d9202629ef201376adf519d795dfb5baaa83fe in C:\openjdk-25 
# Fri, 16 May 2025 21:13:23 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 16 May 2025 21:13:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:67993f619eb734923df34b48b82cc62be3bba8b8a12116cccde4695b2546a3ba`  
		Last Modified: Thu, 15 May 2025 19:27:12 GMT  
		Size: 108.8 MB (108780592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a4019e06e6567532f9b346c4b6ac1ccedc26658952d08a8ce9fd192575fd30e`  
		Last Modified: Fri, 16 May 2025 21:14:04 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc585c8df9d64b97b1ffac6fa24bc283284bfbc270faa6c1b464fa1fa0432f7d`  
		Last Modified: Fri, 16 May 2025 21:14:05 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:915f2422588ead042be2f223cc1b4acb177be94365a6254dd2a77f797e671652`  
		Last Modified: Fri, 16 May 2025 21:14:05 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eec5d40298775cf57d9af6a5bcb1180fb3f6de4ff7539c47ada2350aed707b8`  
		Last Modified: Fri, 16 May 2025 21:14:06 GMT  
		Size: 72.4 KB (72400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10ca80c9ba0fbd14cedd8ce361250403d297674ae9efd2a8aacaedc5cbfee99b`  
		Last Modified: Fri, 16 May 2025 21:14:06 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292def4a5087f2c5e8b405466a20bf2bddc6d5f8b9f34b43ec23971609a1dfbb`  
		Last Modified: Fri, 16 May 2025 21:14:06 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28838afc16c74cf596587946d8fdcd6f6561692626b2fec3316fdd0e6d4ddb1c`  
		Last Modified: Sat, 17 May 2025 00:23:54 GMT  
		Size: 208.9 MB (208920575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3873193e3ac25d860de84c7854bb3ef91e6ffd338e18ed8c6ad849625ffb8440`  
		Last Modified: Fri, 16 May 2025 21:14:08 GMT  
		Size: 4.4 MB (4433214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129dea3b3d5b0ae637dcb83466778eb4948781985f1ca4367ea8452a9237805c`  
		Last Modified: Fri, 16 May 2025 21:14:06 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
