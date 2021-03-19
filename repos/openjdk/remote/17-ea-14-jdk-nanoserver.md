## `openjdk:17-ea-14-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:0ab609b7a0635ff1ecf3f613e27e051cf7bc00505743cf9f05d21f346d1de75b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1817; amd64

### `openjdk:17-ea-14-jdk-nanoserver` - windows version 10.0.17763.1817; amd64

```console
$ docker pull openjdk@sha256:2be7fb198f03acc4767e529f7633c78fca16ed8b69ef138936a962a1d78ea961
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285758422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3ca1f9510754f2ac7e864d1384eb4ce61b6cab513b209a0ebc3e2a729f8c47b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 26 Feb 2021 16:47:31 GMT
RUN Apply image 1809-amd64
# Wed, 10 Mar 2021 17:50:47 GMT
SHELL [cmd /s /c]
# Wed, 10 Mar 2021 17:50:48 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 10 Mar 2021 17:50:49 GMT
USER ContainerAdministrator
# Wed, 10 Mar 2021 17:51:08 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 10 Mar 2021 17:51:08 GMT
USER ContainerUser
# Fri, 19 Mar 2021 19:19:25 GMT
ENV JAVA_VERSION=17-ea+14
# Fri, 19 Mar 2021 19:19:43 GMT
COPY dir:4fc7b435a9bb0f799cfb645c1df4610986b173d8a44747eb2d548c316662fff8 in C:\openjdk-17 
# Fri, 19 Mar 2021 19:20:14 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 19 Mar 2021 19:20:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a11c4ca8f1ba16b6e1395d4523be2215bd0871c2e3e4695b9f2b87bd7472be52`  
		Size: 101.4 MB (101389964 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b1146273d9b624ee892dfcbb3c753523f09f79536a16d63b711cb0027825374a`  
		Last Modified: Wed, 10 Mar 2021 18:33:51 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8c1ac1e6f2d0594fe7e8e0395310c60461fc8ce5183f6a15db964a07b66176e`  
		Last Modified: Wed, 10 Mar 2021 18:33:51 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:050de60c3748a5bfc798f599cadba652e52a162ca31f36b8c783664c11ed224b`  
		Last Modified: Wed, 10 Mar 2021 18:33:54 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e309359702f2d5c4fa7bc854144ad320712050892d017cdfcb58acff4fea2609`  
		Last Modified: Wed, 10 Mar 2021 18:33:50 GMT  
		Size: 66.6 KB (66576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97ecf2dccedb4699a8caf6c19a7a80768c90efb0af5959f1465b00abe8faa12`  
		Last Modified: Wed, 10 Mar 2021 18:33:48 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebe1091c0cc47502da719e0d8a9d1d9e5b31fd406445f08ad6d259e765f33894`  
		Last Modified: Fri, 19 Mar 2021 19:28:17 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a89fb80e2a7b20c932ea18f3ca4db864c8cd6f62f62ba0acdf477cfb58539291`  
		Last Modified: Fri, 19 Mar 2021 19:28:38 GMT  
		Size: 180.7 MB (180665695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f491e1bbfc59191946ddf042c428230fab558fb01aa5a90059291255c853ed`  
		Last Modified: Fri, 19 Mar 2021 19:28:19 GMT  
		Size: 3.6 MB (3629230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e411c8b34d637e37ffdb9a70f629dcaa5928ddc7655f825b67a9062766a4993`  
		Last Modified: Fri, 19 Mar 2021 19:28:19 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
