## `openjdk:25-ea-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:2e2712fabe8c57f9da3925cbbcebe1e9464be86a4d8287f9f4b3fe9b3510c465
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3932; amd64

### `openjdk:25-ea-nanoserver-ltsc2022` - windows version 10.0.20348.3932; amd64

```console
$ docker pull openjdk@sha256:3bc0bbaa7b1cba452c651f532b7bbca1790eeccc4eab573da09bde724fc3b9e8
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.4 MB (341360947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f5b9a98759b4266ccfa50ce9eb01a4d308148024560c4692ae1f02ebfb0a4aa`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Jul 2025 05:15:23 GMT
RUN Apply image 10.0.20348.3932
# Wed, 09 Jul 2025 19:12:18 GMT
SHELL [cmd /s /c]
# Wed, 09 Jul 2025 19:12:19 GMT
ENV JAVA_HOME=C:\openjdk-25
# Wed, 09 Jul 2025 19:12:20 GMT
USER ContainerAdministrator
# Wed, 09 Jul 2025 19:12:22 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 09 Jul 2025 19:12:23 GMT
USER ContainerUser
# Wed, 09 Jul 2025 19:12:24 GMT
ENV JAVA_VERSION=25-ea+30
# Wed, 09 Jul 2025 19:12:31 GMT
COPY dir:3f4870c1d66808f40120812f97095242c2c5faef4fbe09ec60976bc998095719 in C:\openjdk-25 
# Wed, 09 Jul 2025 19:12:37 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 09 Jul 2025 19:12:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b1cf2c299ff70c52cb8ecf52e66d64d5068519867510919d8807ed2c58a54ba2`  
		Last Modified: Tue, 08 Jul 2025 21:55:51 GMT  
		Size: 122.6 MB (122630906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b670139f256b533c51729d4cf34fcf5c4d88d5ba0b157a0a249222ca8b7b623`  
		Last Modified: Wed, 09 Jul 2025 19:13:00 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bae8ae06d96d313979e93cedd0eefc669b90c79f19f7757e05057a731de2312`  
		Last Modified: Wed, 09 Jul 2025 19:13:00 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7be33e190e4c29184822e5d8d8977420ab31f75238168b3e25f8cd30959e955`  
		Last Modified: Wed, 09 Jul 2025 19:13:00 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723c539720220859a9123edfce3b648288c6b12bb6a35066f836fe4a2dbbf183`  
		Last Modified: Wed, 09 Jul 2025 19:13:00 GMT  
		Size: 76.5 KB (76532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a22bf52ccfce71dfe98b7d7c3b6dacb9b8c10b3b7d695e57f281bc0ec3efd85`  
		Last Modified: Wed, 09 Jul 2025 19:13:00 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8850b24a8cb738ea39944174b970bce4faa60f3b22f9f41bcb6879fe1466151b`  
		Last Modified: Wed, 09 Jul 2025 19:13:00 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538742083548f9c7105a9eb41ad10c1d1ba2749b23d62efed2f8839452e5d874`  
		Last Modified: Wed, 09 Jul 2025 21:23:49 GMT  
		Size: 218.5 MB (218529485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:181f644dc4b387b1818136cf484dc62b96e42e2c73ecc8743307f425551c04b2`  
		Last Modified: Wed, 09 Jul 2025 19:13:00 GMT  
		Size: 117.8 KB (117845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:887578a947a84b73b3f9865abcaa657018d914181fe11bfed0e5d2fd702b092f`  
		Last Modified: Wed, 09 Jul 2025 19:13:00 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
