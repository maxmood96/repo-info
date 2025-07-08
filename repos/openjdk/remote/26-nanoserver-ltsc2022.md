## `openjdk:26-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:8809335d1705c691f961d3a4566e6849023a9333746eb4dac6c43c56eb68c7b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `openjdk:26-nanoserver-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull openjdk@sha256:fffc4cd602158c8fe18ee4edc25d891aacb3f0d6123ca6a259083323d68368b9
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.2 MB (341215316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842ac516a9e56112d58f2aa8f0e9270a256951e142cda06f6be840c17edeb9ee`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Jun 2025 00:43:46 GMT
RUN Apply image 10.0.20348.3807
# Mon, 07 Jul 2025 21:05:15 GMT
SHELL [cmd /s /c]
# Mon, 07 Jul 2025 21:05:16 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 07 Jul 2025 21:05:18 GMT
USER ContainerAdministrator
# Mon, 07 Jul 2025 21:05:24 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 07 Jul 2025 21:05:25 GMT
USER ContainerUser
# Mon, 07 Jul 2025 21:05:26 GMT
ENV JAVA_VERSION=26-ea+5
# Mon, 07 Jul 2025 21:05:35 GMT
COPY dir:a8af305eda69ca7e4a97e843a96509e487ef158cc8b5f27ab7de11cd1f4c0ba7 in C:\openjdk-26 
# Mon, 07 Jul 2025 21:05:42 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 07 Jul 2025 21:05:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:96acbf1c6d5b6cc37517502ecbb6a1d2eb55b7615b696401ead868c97a971964`  
		Last Modified: Tue, 10 Jun 2025 20:17:56 GMT  
		Size: 122.5 MB (122540534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf6a0f8055b14c6453a80db1e7dd14158a717a540906945a3f920706fcddc3a`  
		Last Modified: Mon, 07 Jul 2025 21:06:25 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:604ef758906646f10fd5aa3b270c8b9cac78e86590cf8268cfed6b367482b966`  
		Last Modified: Mon, 07 Jul 2025 21:06:25 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2dd202d28bb3f5600a1e8e77fdb49e59ad5513f3079b9c9c686e4a91c1afd93`  
		Last Modified: Mon, 07 Jul 2025 21:06:25 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:999e24764b7f7d9da58951191144097465a7bbff6bc7a6ace4c5c07da042fece`  
		Last Modified: Mon, 07 Jul 2025 21:06:25 GMT  
		Size: 84.8 KB (84804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95c62ba0c92808b47df3e87bdbcf0b47553a261fe58762392ab132bc713642fe`  
		Last Modified: Mon, 07 Jul 2025 21:06:25 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecd63bee7508692f2c72a1d67d88a81dbca08adee187530b2c05999b9dc97d96`  
		Last Modified: Mon, 07 Jul 2025 21:06:25 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946c2602cea3dee0286edac1038b40365941f6a860299c05756775ab931de484`  
		Last Modified: Tue, 08 Jul 2025 00:24:49 GMT  
		Size: 218.5 MB (218485861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c019ead1569e8ed5a6328bece9513348019693a440a3f446be0cc00e1e25aa36`  
		Last Modified: Mon, 07 Jul 2025 21:06:23 GMT  
		Size: 97.9 KB (97936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beb5a9435f6712353d21f2cf5839074ecb6efbf92c91002419165626862c6e0e`  
		Last Modified: Mon, 07 Jul 2025 21:06:23 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
