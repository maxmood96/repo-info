## `openjdk:23-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:78f842e1763a6ed3e5fd7226dc03b971828b1ae32e71d906b2d593458bce6dea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `openjdk:23-jdk-nanoserver-1809` - windows version 10.0.17763.6054; amd64

```console
$ docker pull openjdk@sha256:af0a95e69c2d7d79b371f68589a4df37f40afabc592755cefec5409dbd9fca7a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.5 MB (366493119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f7d1c0cb8337a79233c7e0f490418e93098912048a2cd443ef6d004dc9e91eb`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 03 Jul 2024 00:02:58 GMT
RUN Apply image 10.0.17763.6054
# Wed, 10 Jul 2024 18:13:00 GMT
SHELL [cmd /s /c]
# Wed, 10 Jul 2024 18:13:01 GMT
ENV JAVA_HOME=C:\openjdk-23
# Wed, 10 Jul 2024 18:13:01 GMT
USER ContainerAdministrator
# Wed, 10 Jul 2024 18:13:04 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 10 Jul 2024 18:13:04 GMT
USER ContainerUser
# Wed, 10 Jul 2024 18:13:04 GMT
ENV JAVA_VERSION=23-ea+30
# Wed, 10 Jul 2024 18:13:11 GMT
COPY dir:e9035bffe394ece7120e7b4862d3651b9290e44805dce1863f06816afaf00705 in C:\openjdk-23 
# Wed, 10 Jul 2024 18:13:18 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 10 Jul 2024 18:13:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:53308e1345e8a502fe824770c132f9d645d42108fee87a0708ea8814c901e40d`  
		Last Modified: Tue, 09 Jul 2024 17:42:24 GMT  
		Size: 155.1 MB (155081383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd1672718880b767852e04f61eeaaaabd2863424df049d142ee37968c24b0bbb`  
		Last Modified: Wed, 10 Jul 2024 18:13:26 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02fded4239b792db8fd1f033d0c68b9f88b4a277ed0ea4ae737522e37c200ac3`  
		Last Modified: Wed, 10 Jul 2024 18:13:25 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b16a8328325363d463ff88d8f703e5f3ee0579df5e5e51d5718a5c006091d28`  
		Last Modified: Wed, 10 Jul 2024 18:13:24 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd6370db855394024498230b44df199148a5510b1eadc647a0767c4a25ec2d98`  
		Last Modified: Wed, 10 Jul 2024 18:13:24 GMT  
		Size: 72.2 KB (72229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdebd02e4a22a252bcf329b437617046e9e8e48f7858c36e280defc016520477`  
		Last Modified: Wed, 10 Jul 2024 18:13:23 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1cef88e74d2a96995cd469948a472b1318fda826ce2786e6b2c125a1747c2a`  
		Last Modified: Wed, 10 Jul 2024 18:13:22 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ef1759d184cdc2e1c6a32c6b1a6e3c9be47feaf33f528c17dacca3ce861640`  
		Last Modified: Wed, 10 Jul 2024 18:13:34 GMT  
		Size: 206.1 MB (206059508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0dd12e4f1affb818bf551bca935e863902bf48ed2bd6a1059f2598a21272c45`  
		Last Modified: Wed, 10 Jul 2024 18:13:24 GMT  
		Size: 5.3 MB (5273761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2757c55e5f8131aaf7324f14f772328cc025c8d083b83acaca7f1db35f6670`  
		Last Modified: Wed, 10 Jul 2024 18:13:23 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
