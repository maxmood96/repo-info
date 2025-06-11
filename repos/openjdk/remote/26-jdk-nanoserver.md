## `openjdk:26-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:df28caf37ebfd7e4439dc680af327047947a7c4fafa568d5c222263aaaff3c0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4349; amd64
	-	windows version 10.0.20348.3807; amd64

### `openjdk:26-jdk-nanoserver` - windows version 10.0.26100.4349; amd64

```console
$ docker pull openjdk@sha256:df088b891e92a0e54b6f7633ffc861ba0ae766fc2ebedb5b9fe48746365044ce
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.8 MB (410808962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5db6fd4c10a58b28773340cf290165b0e8b2b5af207088e006f99afd45dff5d0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 07 Jun 2025 15:19:59 GMT
RUN Apply image 10.0.26100.4349
# Tue, 10 Jun 2025 22:15:24 GMT
SHELL [cmd /s /c]
# Tue, 10 Jun 2025 22:15:25 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 10 Jun 2025 22:15:26 GMT
USER ContainerAdministrator
# Tue, 10 Jun 2025 22:15:30 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 10 Jun 2025 22:15:32 GMT
USER ContainerUser
# Tue, 10 Jun 2025 22:15:33 GMT
ENV JAVA_VERSION=26-ea+1
# Tue, 10 Jun 2025 22:15:41 GMT
COPY dir:457747d16cd2fadf291c9e74f2db19f460bea57b69501abf66c1c6daf147dfd2 in C:\openjdk-26 
# Tue, 10 Jun 2025 22:15:48 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 10 Jun 2025 22:15:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:709fa8bff22087ae5c45c65a3b0777eb6ee12afd1b773aece2a322e84b66b1d1`  
		Last Modified: Tue, 10 Jun 2025 22:41:49 GMT  
		Size: 192.1 MB (192082516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:702632f971db72a959168b3a8b42ec77f69de891b9d83ec0948ae80f55f92eaa`  
		Last Modified: Tue, 10 Jun 2025 22:16:35 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4c4e841c594e4f7239403e60fa523ac12b8cd89d9030935f55186dc4e44534`  
		Last Modified: Tue, 10 Jun 2025 22:16:35 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd9888df709e4866304667ac73f2e520690b8b1d9686f3f782d381f0eb44bea`  
		Last Modified: Tue, 10 Jun 2025 22:16:35 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393bbd43e0888b970b2445c49a6261d526c44eb687ff83b376a6f3fadb285ff3`  
		Last Modified: Tue, 10 Jun 2025 22:16:35 GMT  
		Size: 76.4 KB (76353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810847d0774a6e9763e2bdc7e138d2f63165dd04fcaa7ee8f87f46dade8fbd68`  
		Last Modified: Tue, 10 Jun 2025 22:16:35 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75ff8170e02240adf72d27f42fa079f41f2af60700caae4fed012c6540b7a0a2`  
		Last Modified: Tue, 10 Jun 2025 22:16:35 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f8e3deb9afce0f2bfa2cd464b9e74b6f96488b925aecf36555faafdcf12cffb`  
		Last Modified: Wed, 11 Jun 2025 00:25:21 GMT  
		Size: 218.5 MB (218529565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d983b145c4c1dac15649e75246599b80b26172b620bcf998d710dd3f74bbbf67`  
		Last Modified: Tue, 10 Jun 2025 22:16:35 GMT  
		Size: 114.1 KB (114055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:575eba99b12af95c43d4835be4e483efd62fe83c6bdd95563021c9281aa63ee6`  
		Last Modified: Tue, 10 Jun 2025 22:16:35 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:26-jdk-nanoserver` - windows version 10.0.20348.3807; amd64

```console
$ docker pull openjdk@sha256:ececccd8cdb4f1d7c1434dd54b3a5f1c93f37e4f99c65fe24c5918df77df74c7
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.3 MB (341261074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83c7b7bbdcbf6902940f059fbf763ce94a774266fd563672fe31396803e5f6d3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Jun 2025 00:43:46 GMT
RUN Apply image 10.0.20348.3807
# Tue, 10 Jun 2025 22:19:27 GMT
SHELL [cmd /s /c]
# Tue, 10 Jun 2025 22:19:28 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 10 Jun 2025 22:19:29 GMT
USER ContainerAdministrator
# Tue, 10 Jun 2025 22:19:32 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 10 Jun 2025 22:19:32 GMT
USER ContainerUser
# Tue, 10 Jun 2025 22:19:33 GMT
ENV JAVA_VERSION=26-ea+1
# Tue, 10 Jun 2025 22:19:41 GMT
COPY dir:457747d16cd2fadf291c9e74f2db19f460bea57b69501abf66c1c6daf147dfd2 in C:\openjdk-26 
# Tue, 10 Jun 2025 22:19:47 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 10 Jun 2025 22:19:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:96acbf1c6d5b6cc37517502ecbb6a1d2eb55b7615b696401ead868c97a971964`  
		Last Modified: Tue, 10 Jun 2025 20:17:56 GMT  
		Size: 122.5 MB (122540534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14afa113ec78657cc9cf72e26d53fe1eb75f4c00f2fc284b38d4c1ec2790fe7d`  
		Last Modified: Tue, 10 Jun 2025 22:20:27 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fadc3e452bb5594ba009c85b1a9efcadc4c87a424d794dac5a59e4edb75178d9`  
		Last Modified: Tue, 10 Jun 2025 22:20:28 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:862f91d82fe90249e2c0647e195ec95861e5832c2bb1991c719c897037803b6e`  
		Last Modified: Tue, 10 Jun 2025 22:20:28 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb3158898eb90b02ef0a9853dca8b3d947ce54ee678867b555b60e14d7f2dcdc`  
		Last Modified: Tue, 10 Jun 2025 22:20:28 GMT  
		Size: 78.4 KB (78431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4cfcb47da60e4d6090408a44a59cecf7e9418fe98df1ab3afaf12716542993`  
		Last Modified: Tue, 10 Jun 2025 22:20:28 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b0d866b95711c381418eed1b22dcc13c5194777ea09b29185d14f94d606e0e`  
		Last Modified: Tue, 10 Jun 2025 22:20:28 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567773218f9f64461b896feac717bed044e674125b323050343ed00eec3f807d`  
		Last Modified: Wed, 11 Jun 2025 00:25:30 GMT  
		Size: 218.5 MB (218528366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1230070b585512b52cf4f370627869e3f844515e0840d7553301a23278cc282`  
		Last Modified: Tue, 10 Jun 2025 22:20:28 GMT  
		Size: 107.3 KB (107332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54418c4bd08c080cb0decaa9afc8f2862d08972aa780bb4db3836e6bfea6da9c`  
		Last Modified: Tue, 10 Jun 2025 22:20:28 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
