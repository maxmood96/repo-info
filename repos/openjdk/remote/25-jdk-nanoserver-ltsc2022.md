## `openjdk:25-jdk-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:7232a58118aee0bfdf75817fbf17de891eb8deb458db7df482d5b63f8ea16eaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3453; amd64

### `openjdk:25-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.3453; amd64

```console
$ docker pull openjdk@sha256:0711e22c2b5968dff9907838459454e488b36f3c428115fbcffaadd4b0fffbd2
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.5 MB (328509882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:272701b30a85c1e375853dbf5d7490e847eed0ff3f150522136ff48c786fb6fb`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 04 Apr 2025 22:57:50 GMT
RUN Apply image 10.0.20348.3453
# Mon, 14 Apr 2025 23:24:32 GMT
SHELL [cmd /s /c]
# Mon, 14 Apr 2025 23:24:33 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 14 Apr 2025 23:24:34 GMT
USER ContainerAdministrator
# Mon, 14 Apr 2025 23:24:36 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 14 Apr 2025 23:24:37 GMT
USER ContainerUser
# Mon, 14 Apr 2025 23:24:37 GMT
ENV JAVA_VERSION=25-ea+18
# Mon, 14 Apr 2025 23:24:45 GMT
COPY dir:98e2e7765cda338b9693b53f1f8eb40deb194d41cda93e2a54447c0586fe61ce in C:\openjdk-25 
# Mon, 14 Apr 2025 23:24:52 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 14 Apr 2025 23:24:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5caa30147a287e99992660f7f85276c53fe3299503a06c47d476387410721453`  
		Last Modified: Wed, 09 Apr 2025 01:13:36 GMT  
		Size: 120.7 MB (120736312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1271dc6466f60914f513fd58b86a3963158664cbc978ebd558924d38830f49eb`  
		Last Modified: Mon, 14 Apr 2025 23:24:57 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce172a953b02da88a39f83e9e2a560e668585012672e0a3261d04c2f94a0f21`  
		Last Modified: Mon, 14 Apr 2025 23:24:57 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa44aea9556d4463f7e87ded735698719df8dfc0c0b7c32b3647a3715db989f6`  
		Last Modified: Mon, 14 Apr 2025 23:24:57 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b2e2042c88f487a96dffc116642cfd3991b785bafa84e22178e0db5eb329ac`  
		Last Modified: Mon, 14 Apr 2025 23:24:57 GMT  
		Size: 76.3 KB (76291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0bf3300c9f523b2987f709b3633ff61a5e53d6f40892e59ca9effe4797fe8a3`  
		Last Modified: Mon, 14 Apr 2025 23:24:56 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:debad990a6b0334dbf12d87eca164b18cf991b610ebbf985e7e8bd4bf9a2348b`  
		Last Modified: Mon, 14 Apr 2025 23:24:56 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76b463d977dd09f2e70b780d5e2300411837fdd97e46b521d6904db176cdb09`  
		Last Modified: Mon, 14 Apr 2025 23:25:08 GMT  
		Size: 207.6 MB (207583880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03979774dbb19709dc7c914da6827bf4083dc74019a9ca751415b0ab3939e19`  
		Last Modified: Mon, 14 Apr 2025 23:24:56 GMT  
		Size: 107.1 KB (107105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed29696f7bbf7c157e5de30b1a60404af0295efe9896c473f8ae82efa0448c5`  
		Last Modified: Mon, 14 Apr 2025 23:24:56 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
