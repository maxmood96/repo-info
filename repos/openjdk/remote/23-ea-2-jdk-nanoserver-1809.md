## `openjdk:23-ea-2-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:dc2a093c88dcc15ccd2575b65a3d4aa2e7fd3f23eda6243a292b19356e43e1c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5206; amd64

### `openjdk:23-ea-2-jdk-nanoserver-1809` - windows version 10.0.17763.5206; amd64

```console
$ docker pull openjdk@sha256:d06603b43d278b9deae88e5b2c7fd45c461cf0bb72d3edc4be9488c07872cbe8
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.9 MB (305875066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3a0d3947439798b7abb7c3b9f333288a4e1b760087972e1431fc45b500ec17b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 04 Dec 2023 10:54:04 GMT
RUN Apply image 10.0.17763.5206
# Sat, 16 Dec 2023 02:55:55 GMT
SHELL [cmd /s /c]
# Sat, 16 Dec 2023 02:55:56 GMT
ENV JAVA_HOME=C:\openjdk-23
# Sat, 16 Dec 2023 02:55:57 GMT
USER ContainerAdministrator
# Sat, 16 Dec 2023 02:55:59 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Sat, 16 Dec 2023 02:56:00 GMT
USER ContainerUser
# Sat, 16 Dec 2023 02:56:00 GMT
ENV JAVA_VERSION=23-ea+2
# Sat, 16 Dec 2023 02:56:09 GMT
COPY dir:441314f49a5a38f606a8b7ec246e06e2333c273f71f07575ba3181840907923c in C:\openjdk-23 
# Sat, 16 Dec 2023 02:56:15 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Sat, 16 Dec 2023 02:56:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:424f13a93a185a5defe848e7d270655e05233555f51328c0af24b9e70677d037`  
		Last Modified: Tue, 12 Dec 2023 20:02:40 GMT  
		Size: 104.5 MB (104510104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0105f80ff06808ab584fb36977a2bcfd45a140ce3b81fa7dacb01fc778278d8`  
		Last Modified: Sat, 16 Dec 2023 02:56:22 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c45959e3dc3ece98399cdbb226aecc49b7f3212b80674241b61356119db04cd6`  
		Last Modified: Sat, 16 Dec 2023 02:56:21 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d913d4bdcc242de68edcb0249f65886bada5c3ddaf2722ef2f0893f94b7262af`  
		Last Modified: Sat, 16 Dec 2023 02:56:21 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcfb896e9203f4a4b32104d9a76671ccbbe674e34802e8883178e18a52b74095`  
		Last Modified: Sat, 16 Dec 2023 02:56:21 GMT  
		Size: 73.9 KB (73869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5326cdb8755f56cd37538d110ca33eede05bf85557066d6fddbbdc28df941201`  
		Last Modified: Sat, 16 Dec 2023 02:56:19 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba476f77f136810138d3dc9e036d2656dd42589bcc262edab4618453f97e40e`  
		Last Modified: Sat, 16 Dec 2023 02:56:19 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff02d29fb98e5a507083dade6a1aea3d8c7ac341f56f77a3b9f8122090fca1d6`  
		Last Modified: Sat, 16 Dec 2023 02:56:31 GMT  
		Size: 197.4 MB (197392883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fefe0194e4235201a18b46032bfd5898f757878ac1f487d9ed5cacd03851f2`  
		Last Modified: Sat, 16 Dec 2023 02:56:20 GMT  
		Size: 3.9 MB (3891977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d3b13b05077c7fdb68db3014da32949c060130ee4509c31cee689b6f99bae9`  
		Last Modified: Sat, 16 Dec 2023 02:56:19 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
