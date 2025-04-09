## `eclipse-temurin:11-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:b2a4c5397c41aab08e5e6a35f69df117cf7563230233a9a1ab8790c5b24c7683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3453; amd64

### `eclipse-temurin:11-nanoserver-ltsc2022` - windows version 10.0.20348.3453; amd64

```console
$ docker pull eclipse-temurin@sha256:9f50659a33dc7cb06ad87fd8f5bfa854d85519b29ea3c14ddff8003ed23ef9bb
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.5 MB (315492835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf0e1ae6ba8686282d6b45123e25b213a46c61833bc56266ed8d62ec0f5d6b1a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 04 Apr 2025 22:57:50 GMT
RUN Apply image 10.0.20348.3453
# Wed, 09 Apr 2025 04:17:47 GMT
SHELL [cmd /s /c]
# Wed, 09 Apr 2025 04:17:48 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Wed, 09 Apr 2025 04:17:49 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 09 Apr 2025 04:17:49 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 04:17:52 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Apr 2025 04:17:52 GMT
USER ContainerUser
# Wed, 09 Apr 2025 04:17:59 GMT
COPY dir:9a97e9a1ce762bb8542962ee0a2b0ca6fa379668e092b80acfc01b297b3b57a6 in C:\openjdk-11 
# Wed, 09 Apr 2025 04:18:05 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 09 Apr 2025 04:18:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5caa30147a287e99992660f7f85276c53fe3299503a06c47d476387410721453`  
		Last Modified: Wed, 09 Apr 2025 01:13:36 GMT  
		Size: 120.7 MB (120736312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9683628ca8845013c48a6027efaf6727a5b90919f644f3a02262d9fee471c59`  
		Last Modified: Wed, 09 Apr 2025 04:18:12 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39f6bd67fe2292c2a37e1e43d9e5d59f5c8a922ec8d8aeedeaafef6879049327`  
		Last Modified: Wed, 09 Apr 2025 04:18:12 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c113151fd89a92d8bb5b086ee708dc12356213b4e621a45a568bc22e7bf0044`  
		Last Modified: Wed, 09 Apr 2025 04:18:12 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2fb458557294e152c19911ac0bb71350a4182bdb2d4f00778e3a43fd9da5bc`  
		Last Modified: Wed, 09 Apr 2025 04:18:12 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f856d7a5a393e68b03ac916bc7f168c6ae1e1ae90831dd149e7115bb44fac1d4`  
		Last Modified: Wed, 09 Apr 2025 04:18:10 GMT  
		Size: 77.0 KB (76999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c4f67392eb965eea705b34bdc7ac9852cd7ee6d9effb7bcb97b83c3855a12cb`  
		Last Modified: Wed, 09 Apr 2025 04:18:10 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ef0e5d4065ea3bac5e0ab6fe81e59216c88938496a03b4d7c3cff98db5807c0`  
		Last Modified: Wed, 09 Apr 2025 04:18:20 GMT  
		Size: 194.6 MB (194555115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b857b1e25e202212bc10cf8fabfadcd877d1eb55ffac7e4dfd9e9f0f82eb05b`  
		Last Modified: Wed, 09 Apr 2025 04:18:10 GMT  
		Size: 118.2 KB (118241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf70b98fe957ebc27ba955c22340265fae75e9528c27bb503018aa0f201114e`  
		Last Modified: Wed, 09 Apr 2025 04:18:10 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
