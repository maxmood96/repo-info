## `openjdk:24-nanoserver`

```console
$ docker pull openjdk@sha256:847b2a7b85e58b25b971f4d8eb37c452f7d30584a0835ef4dd0d30e2cf9a7a13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3476; amd64
	-	windows version 10.0.20348.3328; amd64
	-	windows version 10.0.17763.7009; amd64

### `openjdk:24-nanoserver` - windows version 10.0.26100.3476; amd64

```console
$ docker pull openjdk@sha256:3ac45f4492fb0646ad155708560578a6bb549924e47e69db908c183c9520e48d
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.0 MB (415024990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3578199173b5b43d3150cb9e810929178a264aa3a8e4dd565aeabb88329c5d4c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Mar 2025 05:48:38 GMT
RUN Apply image 10.0.26100.3476
# Wed, 12 Mar 2025 20:16:27 GMT
SHELL [cmd /s /c]
# Wed, 12 Mar 2025 20:16:27 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 12 Mar 2025 20:16:28 GMT
USER ContainerAdministrator
# Wed, 12 Mar 2025 20:16:31 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 12 Mar 2025 20:16:32 GMT
USER ContainerUser
# Wed, 12 Mar 2025 20:16:33 GMT
ENV JAVA_VERSION=24
# Wed, 12 Mar 2025 20:16:40 GMT
COPY dir:cf5ecdf170ed29d5224593d2b3a510464d2e7297517065c397a2229de8b2a139 in C:\openjdk-24 
# Wed, 12 Mar 2025 20:16:47 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 12 Mar 2025 20:16:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6008a43ec9274f69b461027b7f4e2fe6a71387d40072c0b5b4f0dbbfa688d8a5`  
		Last Modified: Wed, 12 Mar 2025 18:43:31 GMT  
		Size: 206.3 MB (206302205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35cc6622170242b97dec857f04ec214c2eac82ba5cf9e0dc3bd06e085bdbfe86`  
		Last Modified: Wed, 12 Mar 2025 20:16:54 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dbcadbb15be9f8a0826327ed9d3f56a5c8f0dccaeab2a8a7142288ad717a869`  
		Last Modified: Wed, 12 Mar 2025 20:16:54 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a240907a0a0e4138336cee02bdb24df221e01561ef76cf594c581c16c7929aca`  
		Last Modified: Wed, 12 Mar 2025 20:16:54 GMT  
		Size: 1.1 KB (1115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8e536b3da1cacb478c1023a8a9694b308b130b7e74c12db98b67adc336dea6e`  
		Last Modified: Wed, 12 Mar 2025 20:16:54 GMT  
		Size: 76.0 KB (76001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10449b92c264842fdfd8f0b3cf1f43bcd42be6a7acf016a2afd6e7c4f7ec263b`  
		Last Modified: Wed, 12 Mar 2025 20:16:52 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b37f863d986ff7053004a96ef0d1fb0418f865377a19b2d6e1097c271045ffa6`  
		Last Modified: Wed, 12 Mar 2025 20:16:52 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da13f25d9b62b08dc3de933d68b6700a2bc44bf5a47bac1a1bd6fe2c8fe94455`  
		Last Modified: Wed, 12 Mar 2025 20:17:03 GMT  
		Size: 208.5 MB (208526023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367130c979c4c8cefff1131124589a33b26cc0b785e65d97a0d07a0bceb82030`  
		Last Modified: Wed, 12 Mar 2025 20:16:52 GMT  
		Size: 114.3 KB (114322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a30428d0fa016312a7681999e9f8811fa4353d048b9e1e8f1fa6ad278da2ddfe`  
		Last Modified: Wed, 12 Mar 2025 20:16:52 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:24-nanoserver` - windows version 10.0.20348.3328; amd64

```console
$ docker pull openjdk@sha256:f4c93638f263137b23a65a478bd44619b0e00d7dee5267f8ee0f58204540f916
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.4 MB (329412851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04bb256eca5965ab27704bfe1a142cb75aa91944c140a48bae98fad33dfbb0d8`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 06 Mar 2025 10:30:39 GMT
RUN Apply image 10.0.20348.3328
# Wed, 12 Mar 2025 19:20:36 GMT
SHELL [cmd /s /c]
# Wed, 12 Mar 2025 19:20:36 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 12 Mar 2025 19:20:37 GMT
USER ContainerAdministrator
# Wed, 12 Mar 2025 19:20:39 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 12 Mar 2025 19:20:40 GMT
USER ContainerUser
# Wed, 12 Mar 2025 19:20:40 GMT
ENV JAVA_VERSION=24
# Wed, 12 Mar 2025 19:20:48 GMT
COPY dir:cf5ecdf170ed29d5224593d2b3a510464d2e7297517065c397a2229de8b2a139 in C:\openjdk-24 
# Wed, 12 Mar 2025 19:20:52 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 12 Mar 2025 19:20:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:47ec0d45ee7716f773dfebb62d84eb3893d3af9baf9c799960566b016a17e330`  
		Last Modified: Wed, 12 Mar 2025 02:22:56 GMT  
		Size: 120.7 MB (120695547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f50c106cbea715bd596ac3bd3d4d9d38b9966b18be67b816cf0a708d1ce7fe4`  
		Last Modified: Wed, 12 Mar 2025 19:20:56 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e67bf0975e1011e1fa3c59572f5570d47501afc812266ff0132db3a8a07164c8`  
		Last Modified: Wed, 12 Mar 2025 19:20:56 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4908a201cd9667c15b0acb5a9d9c96079006f12cc6d32601cfd9b35235f40d`  
		Last Modified: Wed, 12 Mar 2025 19:20:56 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b2454158d0933710509175e5f75438c2df026004d9a5a808b4e582461d322b`  
		Last Modified: Wed, 12 Mar 2025 19:20:56 GMT  
		Size: 77.9 KB (77855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c96def51a2e52584a23c329bcc7228bf36d5bd1924f2da610c9d06f8733550e`  
		Last Modified: Wed, 12 Mar 2025 19:20:55 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02ad963c115761292c5bc46519839dff88f092af97710d166c278fcdf15b9a54`  
		Last Modified: Wed, 12 Mar 2025 19:20:55 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb83d082dcf1cc7132c57a32ee69a8175e4c85bf0a42149da548768e36cdb85`  
		Last Modified: Wed, 12 Mar 2025 19:21:08 GMT  
		Size: 208.5 MB (208527151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:352e9248248044ed1d678062f7d8834ae922359fb9e0dd044b7c4c365afe5606`  
		Last Modified: Wed, 12 Mar 2025 19:20:55 GMT  
		Size: 106.1 KB (106078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ee0cb13e0f796f305a995a793edfb9f6b5a4a1823af092c23916ae25858d7ef`  
		Last Modified: Wed, 12 Mar 2025 19:20:55 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:24-nanoserver` - windows version 10.0.17763.7009; amd64

```console
$ docker pull openjdk@sha256:5e6dbf9ad777f6bd031f5cafcf9544214f3c68835bce7abe50499e98016e976e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.9 MB (319929273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c03140cc676c836e6a4418c7a2255568164d910a4485c36db006acaa753f814`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Wed, 12 Mar 2025 20:19:43 GMT
SHELL [cmd /s /c]
# Wed, 12 Mar 2025 20:19:45 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 12 Mar 2025 20:19:46 GMT
USER ContainerAdministrator
# Wed, 12 Mar 2025 20:19:49 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 12 Mar 2025 20:19:49 GMT
USER ContainerUser
# Wed, 12 Mar 2025 20:19:50 GMT
ENV JAVA_VERSION=24
# Wed, 12 Mar 2025 20:19:57 GMT
COPY dir:cf5ecdf170ed29d5224593d2b3a510464d2e7297517065c397a2229de8b2a139 in C:\openjdk-24 
# Wed, 12 Mar 2025 20:20:04 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 12 Mar 2025 20:20:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aaa9cc59fc8245982583e2ba7066554376104e0b255cd2189e1a6374d5e1738`  
		Last Modified: Wed, 12 Mar 2025 20:20:09 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e85c989974e4505e3f203901697f3c42acf1fc3e77f0183e5bedde0a901fbae8`  
		Last Modified: Wed, 12 Mar 2025 20:20:08 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e827a05e4017ee6f1b8d009f5cce2d2685fb011003322cb3dfbfffa7f5a4868`  
		Last Modified: Wed, 12 Mar 2025 20:20:08 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b68463103fd220685a3ddda2b8047014ce4654617abeeafa5966142ae3f4570`  
		Last Modified: Wed, 12 Mar 2025 20:20:08 GMT  
		Size: 71.0 KB (71003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f76d556ef11c4fc632df2fdfb223dc8c85d724ab5c2c2bab52c1db4ce926758`  
		Last Modified: Wed, 12 Mar 2025 20:20:07 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20005c9a7f532f4d32c3631a14d480b7a786c211d8a42724b7202751a262e883`  
		Last Modified: Wed, 12 Mar 2025 20:20:07 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138ba1ff9b4da4fcd74b37b19c85b6155e019764ffe20a1906857a19dce85cce`  
		Last Modified: Wed, 12 Mar 2025 20:20:19 GMT  
		Size: 208.5 MB (208527162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec5ef580ef4bbde578c0b1825b550973b1842fba060c45c4eed2732975b076f`  
		Last Modified: Wed, 12 Mar 2025 20:20:08 GMT  
		Size: 4.4 MB (4417176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff52af6f5f82f493d0d13e7c822bebf803b3d70c419e93a72f0411abe861c8c9`  
		Last Modified: Wed, 12 Mar 2025 20:20:07 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
