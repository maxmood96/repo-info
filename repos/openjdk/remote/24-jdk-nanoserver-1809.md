## `openjdk:24-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:bc1a4ee943b04134aee2f2396e27cea6df414d73f62872ae38c011b1b54be706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `openjdk:24-jdk-nanoserver-1809` - windows version 10.0.17763.7009; amd64

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
