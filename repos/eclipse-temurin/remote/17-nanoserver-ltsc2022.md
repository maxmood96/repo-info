## `eclipse-temurin:17-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:5b3f6413d5ebd412fed7dda922f28e2a133b8e8a1a63e7b569c0956dd676da2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.887; amd64

### `eclipse-temurin:17-nanoserver-ltsc2022` - windows version 10.0.20348.887; amd64

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
