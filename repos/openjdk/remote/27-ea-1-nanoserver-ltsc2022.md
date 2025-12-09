## `openjdk:27-ea-1-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:3b238ad94d62226f631249658a8355b09094eaac355700d6c7c89713934c643b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `openjdk:27-ea-1-nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull openjdk@sha256:528a5e00b428dc03fa753aedaa0b7fddf104fe0f9ca240863a068a4d41365fff
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.8 MB (351784427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2828e68fcb0314ef536d7b56da6ce1283d771245d4db70ec8116c278b9e66d56`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Tue, 09 Dec 2025 21:12:58 GMT
SHELL [cmd /s /c]
# Tue, 09 Dec 2025 21:16:21 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 09 Dec 2025 21:16:22 GMT
USER ContainerAdministrator
# Tue, 09 Dec 2025 21:16:23 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 09 Dec 2025 21:16:23 GMT
USER ContainerUser
# Tue, 09 Dec 2025 21:16:24 GMT
ENV JAVA_VERSION=27-ea+1
# Tue, 09 Dec 2025 21:16:32 GMT
COPY dir:19d14afdca91419101de212977382a6561545d70f03a447b9d85c65ba4bb2f53 in C:\openjdk-27 
# Tue, 09 Dec 2025 21:16:37 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 09 Dec 2025 21:16:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6081bd6804178009789fc41fc7b5b028534888b64e10cd0ca092b3f3c75127c3`  
		Last Modified: Tue, 09 Dec 2025 21:13:37 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:679983edeb8f1455b677bb197160b1d516ab29cc4ef194ace2635fd28c717c1a`  
		Last Modified: Tue, 09 Dec 2025 21:17:04 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd1a00136978127bbbaadd9b742fd91a3bc3dcd033add9f05df697f998f1352`  
		Last Modified: Tue, 09 Dec 2025 21:17:04 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44272195f2d7de74b7d8bdb387c265268e9b8dce3de34a8d5c9f169edcdf3ec0`  
		Last Modified: Tue, 09 Dec 2025 21:17:04 GMT  
		Size: 77.0 KB (77001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb9e3e9e8623857384759752f061d59ba4e5110d572e362d6001369a53888b8f`  
		Last Modified: Tue, 09 Dec 2025 21:17:04 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:793650abccca0582d5440fdda1eb5ae1a25fe527f5d2f52511eeceecfe96cd53`  
		Last Modified: Tue, 09 Dec 2025 21:17:04 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8717a899e2122d842da1b2befef443a177b79e834434690a21845dd034c20d`  
		Last Modified: Tue, 09 Dec 2025 21:17:10 GMT  
		Size: 225.2 MB (225224853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a098944add29e910f88422f4b8f58d1db448d8d23009a6a5462a85f8b791dd0`  
		Last Modified: Tue, 09 Dec 2025 21:17:04 GMT  
		Size: 117.9 KB (117868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f09eb5863f556db33ed68e3b467a3e6d91cef4b87e50b2a82dafdbd8ad2d3f4`  
		Last Modified: Tue, 09 Dec 2025 22:20:31 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
