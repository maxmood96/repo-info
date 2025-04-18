## `eclipse-temurin:8u442-b06-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:7139b0c6d9e7fd3d48c3f723cea649a5c473c9c27793063e2931ec4dd3b52edf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3781; amd64
	-	windows version 10.0.20348.3566; amd64
	-	windows version 10.0.17763.7249; amd64

### `eclipse-temurin:8u442-b06-jre-nanoserver` - windows version 10.0.26100.3781; amd64

```console
$ docker pull eclipse-temurin@sha256:c086fb65cadd30ad3648255c288253936087fa7791d3104545df0600896af468
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230871628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81d0b64ed1e8fa0e32951194058e118ef35f15de482b76b879f96b647e2d2f0a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 15 Apr 2025 09:41:29 GMT
RUN Apply image 10.0.26100.3781
# Fri, 18 Apr 2025 04:17:11 GMT
SHELL [cmd /s /c]
# Fri, 18 Apr 2025 04:17:12 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Fri, 18 Apr 2025 04:17:14 GMT
ENV JAVA_HOME=C:\openjdk-8
# Fri, 18 Apr 2025 04:17:15 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 04:17:20 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 18 Apr 2025 04:17:21 GMT
USER ContainerUser
# Fri, 18 Apr 2025 04:17:26 GMT
COPY dir:5687adced9ba5f2555526fe07fa3e848c7771941703db13fa4b29a0f81d58070 in C:\openjdk-8 
# Fri, 18 Apr 2025 04:17:31 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:c012166dfdb57168c954f830d80f494e556a2c597b84901e39aefb605b5e1a02`  
		Last Modified: Thu, 17 Apr 2025 02:52:17 GMT  
		Size: 190.1 MB (190142038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78b2352202160345b8d24370a5c8b6979c17edd474a58cc34b583c607e8f401`  
		Last Modified: Fri, 18 Apr 2025 04:17:35 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d83647f952f5e831c597de15465c8e2af9162bf229505a766d60737a35fe1bb`  
		Last Modified: Fri, 18 Apr 2025 04:17:35 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14951b2adaf7fc0394c4b602a328b26dcb984fd7b51203a150015a4185147423`  
		Last Modified: Fri, 18 Apr 2025 04:17:35 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c002918b74cd6710d2a6e3e3caa26fde517d88af44050c1e15f240d095682cb4`  
		Last Modified: Fri, 18 Apr 2025 04:17:34 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638d75622150c5c83138fec9d917d9389df3515e9b6b7feb1a7a9609a8a13f99`  
		Last Modified: Fri, 18 Apr 2025 04:17:34 GMT  
		Size: 78.5 KB (78540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba615f9f70690cab3cb3b0395e771bf31a2049b473e42aea2ebea1b1c56c932`  
		Last Modified: Fri, 18 Apr 2025 04:17:34 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:349b3b48f600d984770f2c6a4f449a33257d8cbce2d48577ab7ff10c243f4ecf`  
		Last Modified: Fri, 18 Apr 2025 04:17:37 GMT  
		Size: 40.6 MB (40552726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3ee4b2297e79195d5d3062572cbf30335fe760b60b86528002a9fca84a1ab5`  
		Last Modified: Fri, 18 Apr 2025 04:17:34 GMT  
		Size: 93.1 KB (93086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8u442-b06-jre-nanoserver` - windows version 10.0.20348.3566; amd64

```console
$ docker pull eclipse-temurin@sha256:a02b4f4cb22f170b6bbd65ab31fa9b50ad8686e5728d88ce3d099e89182e4dd5
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.3 MB (163280912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2f67d5d875959397dc09602de018c6926612febe7244abf7101831773e081d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 16 Apr 2025 03:28:26 GMT
RUN Apply image 10.0.20348.3566
# Fri, 18 Apr 2025 04:16:03 GMT
SHELL [cmd /s /c]
# Fri, 18 Apr 2025 04:16:04 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Fri, 18 Apr 2025 04:16:05 GMT
ENV JAVA_HOME=C:\openjdk-8
# Fri, 18 Apr 2025 04:16:05 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 04:16:08 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 18 Apr 2025 04:16:08 GMT
USER ContainerUser
# Fri, 18 Apr 2025 04:16:12 GMT
COPY dir:5687adced9ba5f2555526fe07fa3e848c7771941703db13fa4b29a0f81d58070 in C:\openjdk-8 
# Fri, 18 Apr 2025 04:16:17 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:905464f5b09ec7543cfd4984311153c5e327937892d0e49e145f6b363cf68441`  
		Last Modified: Wed, 16 Apr 2025 23:30:29 GMT  
		Size: 122.5 MB (122539088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5c77a4652f8ffaa8ad7f446a5ca0ef750b1a4d72271faaa417c8dea5acc870`  
		Last Modified: Fri, 18 Apr 2025 04:16:22 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f451e9dc45652475f076cc82c54f0c465367cd538d60084bbb5c217a2fa7f3e`  
		Last Modified: Fri, 18 Apr 2025 04:16:22 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce243a9083e9f2e73524538bba29f12545b030c662442982cb0d944444016385`  
		Last Modified: Fri, 18 Apr 2025 04:16:22 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a2990e256e47f1dc5315dcc9b4fe3e074af6eed669a8d73c422bc04398914f1`  
		Last Modified: Fri, 18 Apr 2025 04:16:21 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86de86d2ea71ee40123a525d17b21c0beede395e4657a069e6633c8f069f3eac`  
		Last Modified: Fri, 18 Apr 2025 04:16:21 GMT  
		Size: 77.3 KB (77332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906aec2f9cdd615d84b281003539ea16b5097d9a65546a7e77a037343fdc27e4`  
		Last Modified: Fri, 18 Apr 2025 04:16:21 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8efc4cc63b438109ec0ff0c40296dcbcc43939f4e0e694bb0f9423b0b85e3800`  
		Last Modified: Fri, 18 Apr 2025 04:16:24 GMT  
		Size: 40.6 MB (40552511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd331e0be33c88c7ce9b6088752065c5a9a6cf6e122c015609960e8c92f8bac`  
		Last Modified: Fri, 18 Apr 2025 04:16:21 GMT  
		Size: 106.8 KB (106830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8u442-b06-jre-nanoserver` - windows version 10.0.17763.7249; amd64

```console
$ docker pull eclipse-temurin@sha256:52774750386a6406c98c7b22e2d51297d67d0ceab49750b3a720b794f99e072e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.5 MB (149483805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4834ff5193ed43f310b26f1389d79066ff49f5df85760e3d889d1ed2401830bb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 15 Apr 2025 01:30:17 GMT
RUN Apply image 10.0.17763.7249
# Fri, 18 Apr 2025 04:15:05 GMT
SHELL [cmd /s /c]
# Fri, 18 Apr 2025 04:15:07 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Fri, 18 Apr 2025 04:15:07 GMT
ENV JAVA_HOME=C:\openjdk-8
# Fri, 18 Apr 2025 04:15:08 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 04:15:11 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 18 Apr 2025 04:15:11 GMT
USER ContainerUser
# Fri, 18 Apr 2025 04:15:14 GMT
COPY dir:5687adced9ba5f2555526fe07fa3e848c7771941703db13fa4b29a0f81d58070 in C:\openjdk-8 
# Fri, 18 Apr 2025 04:15:18 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:559b23b3f8a9b205cc3c87a98df1233325878f8360cece22c8822b2a5fc8731a`  
		Last Modified: Wed, 16 Apr 2025 23:46:26 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b37b0eced1360f181fac38b2f2f0c4a981da7db22eb9d796506a19bc53093b`  
		Last Modified: Fri, 18 Apr 2025 04:15:23 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30aced64f1fd02e0d422985800ad389b49805ef857fb4d924af650d127417a52`  
		Last Modified: Fri, 18 Apr 2025 04:15:23 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b29175cff2d29bedf4f23ab8467bfc69bc3dbe3b24b57e10a72cb510b4e0c2e`  
		Last Modified: Fri, 18 Apr 2025 04:15:23 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5dce7ad54b3da46e4369cf49da7c40df178469f87bfc2a2d15c2813a518d53f`  
		Last Modified: Fri, 18 Apr 2025 04:15:22 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ccb50adb37cf49af155f7524bb3f22dd7f63e4afd925690b9332f9f95faf02`  
		Last Modified: Fri, 18 Apr 2025 04:15:22 GMT  
		Size: 73.5 KB (73459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40acafb373b60f153cab01e55eeb3a93b33becf347a8fe7e65bd7f5ce27d82e1`  
		Last Modified: Fri, 18 Apr 2025 04:15:22 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8704a29f332693a188821acf3b59f071a4ea94cf4a1aa6732504e6da661254`  
		Last Modified: Fri, 18 Apr 2025 04:15:25 GMT  
		Size: 40.6 MB (40552354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:305677797e3285ef74df871e66816a815c224e5902d63085d9bd3a909656438d`  
		Last Modified: Fri, 18 Apr 2025 04:15:22 GMT  
		Size: 100.6 KB (100569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
