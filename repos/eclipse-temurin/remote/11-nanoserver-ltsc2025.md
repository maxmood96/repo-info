## `eclipse-temurin:11-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:415dd7f65875e4d122f7763d61a61c6b0497c255cd4528a02eefad468d0a2fc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32690; amd64

### `eclipse-temurin:11-nanoserver-ltsc2025` - windows version 10.0.26100.32690; amd64

```console
$ docker pull eclipse-temurin@sha256:c7c2baa5b5e000390c8784f8d741e393755b7162c3210de0d3cdb4f4ab196625
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.7 MB (394681991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eecae6d8c0a0bcd68235b4ad8141d50edc04cb486b4a2750ebda518d76b9d3a5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Apr 2026 06:39:57 GMT
RUN Apply image 10.0.26100.32690
# Wed, 29 Apr 2026 23:09:30 GMT
SHELL [cmd /s /c]
# Wed, 29 Apr 2026 23:09:30 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Wed, 29 Apr 2026 23:09:30 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 29 Apr 2026 23:09:31 GMT
USER ContainerAdministrator
# Wed, 29 Apr 2026 23:09:38 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 29 Apr 2026 23:09:39 GMT
USER ContainerUser
# Wed, 29 Apr 2026 23:10:10 GMT
COPY dir:508f69ae524938b28a83a19a9aeade10facf00325b620c7a836698644d966097 in C:\openjdk-11 
# Wed, 29 Apr 2026 23:10:18 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 29 Apr 2026 23:10:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8af320c3b6d19296bcc7947e3beb8bc0c69cb12143db52efe988dc998ac088dc`  
		Last Modified: Tue, 14 Apr 2026 21:00:37 GMT  
		Size: 199.7 MB (199717094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f140e62df6d3d335bf8a75dc0b3cdd1358c8581cf4944b074b39e5d11f9373c`  
		Last Modified: Wed, 29 Apr 2026 23:10:24 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c389429cd25e7004815a252f8cdce92d85e97df2c9c5a0ed008b5733dc797a6`  
		Last Modified: Wed, 29 Apr 2026 23:10:24 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf5570b6ef37c81ade56533f80fb075eca3facb8cdb9e5ae404fd4388ccb688`  
		Last Modified: Wed, 29 Apr 2026 23:10:23 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531a81b09bc239f85119f9e95891e9443ff23ddadf5df3cba79ca613f65b53bb`  
		Last Modified: Wed, 29 Apr 2026 23:10:23 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e988a48a5ecddc2557ccfd064a213598d218891dddad9ed82c2a1f805ea909d`  
		Last Modified: Wed, 29 Apr 2026 23:10:22 GMT  
		Size: 70.5 KB (70469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68d5aa71bbcffd31d8093c142f357986f9dce5ebd7106377bfe133532bfe76e7`  
		Last Modified: Wed, 29 Apr 2026 23:10:22 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d43e482929cf547b4da411882b611a5e306175656e48f59e7b03e522790ee2e6`  
		Last Modified: Wed, 29 Apr 2026 23:10:33 GMT  
		Size: 194.8 MB (194785155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5ed32f76f91af18aced1ae93f0ab48c75346cff78078c5d546fbd08f06c18cb`  
		Last Modified: Wed, 29 Apr 2026 23:10:22 GMT  
		Size: 102.8 KB (102845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d1a35f5af32ed9cb7321a1a0d0d160a276422c10387315dde3968b697eaad2c`  
		Last Modified: Wed, 29 Apr 2026 23:10:22 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
