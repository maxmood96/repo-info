## `eclipse-temurin:17-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:7eef5a3c5c7f8bd04345ee79b42df482e10a2c97afce82c327fe27e08adf8e72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.887; amd64
	-	windows version 10.0.17763.3287; amd64

### `eclipse-temurin:17-jdk-nanoserver` - windows version 10.0.20348.887; amd64

```console
$ docker pull eclipse-temurin@sha256:2f618752d2beeda6b536802dbd72855b6c77b9cc135763a82d618fe2a226f82e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.6 MB (303593117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121f982f4990504acab49dbd35904a8096f4f8de3eb784c0410692d1b9d43820`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Aug 2022 18:05:23 GMT
RUN Apply image 10.0.20348.887
# Wed, 10 Aug 2022 16:28:17 GMT
SHELL [cmd /s /c]
# Wed, 10 Aug 2022 16:32:05 GMT
ENV JAVA_VERSION=jdk-17.0.4+8
# Wed, 10 Aug 2022 16:32:06 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 10 Aug 2022 16:32:08 GMT
USER ContainerAdministrator
# Wed, 10 Aug 2022 16:32:28 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Aug 2022 16:32:29 GMT
USER ContainerUser
# Wed, 10 Aug 2022 16:32:45 GMT
COPY dir:be8ac85d984fd6d07ec942e6824366b313a501643dad7e29e6805d4aab47b44c in C:\openjdk-17 
# Wed, 10 Aug 2022 16:33:03 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 10 Aug 2022 16:33:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2ebf439f800cd4c1fccaf4a0545e6bff60caa5141295c8ab81f6c525073c423d`  
		Size: 118.1 MB (118088450 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5f1e06146ab0490d235fe89786637467a4b71853ee428e8740ea6efbc536c47c`  
		Last Modified: Wed, 10 Aug 2022 16:48:40 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3de61c52bad8488967f80c4db87303748e0f7967786da445f0edb64a6fd10b86`  
		Last Modified: Wed, 10 Aug 2022 16:50:08 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb2015012758b67ef5b3aefa0e59ad535b3bb6c9fa0cdc98321ae05bd071d057`  
		Last Modified: Wed, 10 Aug 2022 16:50:08 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06f276d89c88fa27e7993ebe8a765713e068656b5a3d94b7a249867a35814107`  
		Last Modified: Wed, 10 Aug 2022 16:50:08 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c98625edb3795a1afb19c1dd0023ee7cb80d7845ade665227dfcd9293b45f13f`  
		Last Modified: Wed, 10 Aug 2022 16:50:05 GMT  
		Size: 85.1 KB (85090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e687c5eeeb1d78994958244a411c33da1cfe3bf866bfc14442931dc2cdde9d89`  
		Last Modified: Wed, 10 Aug 2022 16:50:05 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:539d76bd9c2f91fc0f5bbf02c7bc4424a6df5644933d0d567515e6d958aced3c`  
		Last Modified: Wed, 10 Aug 2022 16:50:23 GMT  
		Size: 185.3 MB (185326844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41d8f0a69c8d384799409039db31325a60f6218d8b59970c272eae21e71559b`  
		Last Modified: Wed, 10 Aug 2022 16:50:06 GMT  
		Size: 85.9 KB (85882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:851741829428cf5d8b24d0d22b270efe0d8c87ddba89d445561fa60ab9f22153`  
		Last Modified: Wed, 10 Aug 2022 16:50:05 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jdk-nanoserver` - windows version 10.0.17763.3287; amd64

```console
$ docker pull eclipse-temurin@sha256:a0b495d26ceb33782686f6ebc34e769e1d4c1b2b416c1772892a9002b7d22273
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.3 MB (292251141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed34968a9bdd0d25a9aa6e129d1b5b0c31e05d5bc83596aafdd5b9281873e28a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Aug 2022 18:08:38 GMT
RUN Apply image 10.0.17763.3287
# Wed, 10 Aug 2022 15:57:07 GMT
SHELL [cmd /s /c]
# Wed, 10 Aug 2022 16:15:01 GMT
ENV JAVA_VERSION=jdk-17.0.4+8
# Wed, 10 Aug 2022 16:15:02 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 10 Aug 2022 16:15:03 GMT
USER ContainerAdministrator
# Wed, 10 Aug 2022 16:15:12 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Aug 2022 16:15:12 GMT
USER ContainerUser
# Wed, 10 Aug 2022 16:15:27 GMT
COPY dir:be8ac85d984fd6d07ec942e6824366b313a501643dad7e29e6805d4aab47b44c in C:\openjdk-17 
# Wed, 10 Aug 2022 16:15:40 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 10 Aug 2022 16:15:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5c9d6483dab113d2d9b50fdf3156622aa2ec3d6faaed5664d15a5568032d1714`  
		Size: 103.2 MB (103204200 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0f4438539876006761cb687527bd8cb94cc7a273cf8bb47563981044f2e1771e`  
		Last Modified: Wed, 10 Aug 2022 16:38:40 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8036b9d6d653f3f49c26c75410a8bc5fa7343a801bdd59844aa0af69c4fc5d27`  
		Last Modified: Wed, 10 Aug 2022 16:44:11 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91fc4dad1fb9cdc0eb7d42893a9adf6aa618a5f2368b429838f4f4584a320b72`  
		Last Modified: Wed, 10 Aug 2022 16:44:11 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8082b31e68276496e65afb15a5c0e469d935d91cc39d500ced948654c5e28525`  
		Last Modified: Wed, 10 Aug 2022 16:44:12 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9b55f1dc603701feff149984c13ed1bb2a780e935b3a967ea6e2b257d9bf79`  
		Last Modified: Wed, 10 Aug 2022 16:44:09 GMT  
		Size: 74.0 KB (73984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9c75f6dbbdc460cf364a2088e3a384a624fbdb085141d8fe768d0b64c0ece7`  
		Last Modified: Wed, 10 Aug 2022 16:44:09 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52e00e66b4749caa0fc829d9567bcbe127edd5574fc5d24f545fe9f825eedf7`  
		Last Modified: Wed, 10 Aug 2022 16:44:29 GMT  
		Size: 185.3 MB (185341991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba70e86a78a88b58ca49909fcc46d5e7fb3f83d7386dd84b83f6cce728b816d7`  
		Last Modified: Wed, 10 Aug 2022 16:44:10 GMT  
		Size: 3.6 MB (3624064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73eb12d6490d21cf23b2369c8bf4ea984e35e011e3d6156772ec02698e559a93`  
		Last Modified: Wed, 10 Aug 2022 16:44:09 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
