## `eclipse-temurin:11-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:dbc8bd207ec9584d18b10bf1f209f25761171a9e3533332a0b3b51b44baf5c13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6905; amd64

### `eclipse-temurin:11-nanoserver-ltsc2025` - windows version 10.0.26100.6905; amd64

```console
$ docker pull eclipse-temurin@sha256:988c8da0163f2dac9a521f6d63213c78a71ae1dd879def30dd322c060ea91733
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.9 MB (388891936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9308b49283e9c4076eb1228d17b80cfd27177a149f0161ac9baad93ec600faf`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 22 Oct 2025 07:22:01 GMT
RUN Apply image 10.0.26100.6905
# Sat, 08 Nov 2025 19:18:10 GMT
SHELL [cmd /s /c]
# Sat, 08 Nov 2025 19:18:10 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Sat, 08 Nov 2025 19:18:11 GMT
ENV JAVA_HOME=C:\openjdk-11
# Sat, 08 Nov 2025 19:18:11 GMT
USER ContainerAdministrator
# Sat, 08 Nov 2025 19:18:17 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Sat, 08 Nov 2025 19:18:17 GMT
USER ContainerUser
# Sat, 08 Nov 2025 19:18:41 GMT
COPY dir:207a50c3961430a3231a748eb9ce354eec00313f0753b2d5e8f279d3afd46cd8 in C:\openjdk-11 
# Sat, 08 Nov 2025 19:18:47 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Sat, 08 Nov 2025 19:18:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9188956580c47f583c927f17e42f8825823890544237141f21ca4ef10ea55e60`  
		Last Modified: Fri, 24 Oct 2025 11:13:56 GMT  
		Size: 194.0 MB (194029378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6749df2eb6e260adb92966ccbcfdce7c6b2e7f739754baa421454756f63ca8e4`  
		Last Modified: Sat, 08 Nov 2025 19:19:15 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:500183312b00eb6e44f07b890152c7ac17c9a0a116838d9db6c846fc206e8af4`  
		Last Modified: Sat, 08 Nov 2025 19:19:15 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a090a598bc0bc63aa7cd7c04cef7b0656777c2053aad35de323aefdbaffd0cee`  
		Last Modified: Sat, 08 Nov 2025 19:19:15 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1918fe6407e68eaef97faed9c448cb1ab6d3e0954a6b6f94bd8673e1a11cb710`  
		Last Modified: Sat, 08 Nov 2025 19:19:16 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4637f094d55ef656dda0f5653970cd2a53d6b143407ee8c4c364db9d8939d0c3`  
		Last Modified: Sat, 08 Nov 2025 19:19:16 GMT  
		Size: 70.7 KB (70738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b757f8e9bee5271a896df0e72cca61a379892fbf7506232b2e1b42ac67d0876e`  
		Last Modified: Sat, 08 Nov 2025 19:19:16 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d34cf50423dc69551bc7d868ebb5dda54e9752ac5be4dfa869d93d3dadb90a9`  
		Last Modified: Sat, 08 Nov 2025 22:13:08 GMT  
		Size: 194.7 MB (194671148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed5ef562eb2d1da29296d93c26cad2e5deb47496f7678d43f076c189384f7b99`  
		Last Modified: Sat, 08 Nov 2025 19:19:17 GMT  
		Size: 114.3 KB (114339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:824ae74e3f9b414a09f868acd3be15a36831c0a8964930265296d573859b5f81`  
		Last Modified: Sat, 08 Nov 2025 19:19:17 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
