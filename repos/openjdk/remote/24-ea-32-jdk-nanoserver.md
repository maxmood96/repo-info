## `openjdk:24-ea-32-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:994b7441aa5f4699669d7b40a17151403c049e9c3813c49198a0cd02fc2fedcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `openjdk:24-ea-32-jdk-nanoserver` - windows version 10.0.26100.2894; amd64

```console
$ docker pull openjdk@sha256:7c418f94525150b0de229c87baa48ab4eff9c7b16637d0296a035e881323bf34
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.7 MB (407729479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f19c4e3b6e5fae62e771d6d5db18ed2f4390a5f72d700ee4ef7fae98d5c6c9ac`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Jan 2025 02:49:59 GMT
RUN Apply image 10.0.26100.2894
# Thu, 23 Jan 2025 23:12:13 GMT
SHELL [cmd /s /c]
# Thu, 23 Jan 2025 23:12:13 GMT
ENV JAVA_HOME=C:\openjdk-24
# Thu, 23 Jan 2025 23:12:14 GMT
USER ContainerAdministrator
# Thu, 23 Jan 2025 23:12:16 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Thu, 23 Jan 2025 23:12:17 GMT
USER ContainerUser
# Thu, 23 Jan 2025 23:12:17 GMT
ENV JAVA_VERSION=24-ea+32
# Thu, 23 Jan 2025 23:12:24 GMT
COPY dir:86d923ef445b254beb0a3a098fc78a6b4825f40d8c18f13f837cc4a7df771680 in C:\openjdk-24 
# Thu, 23 Jan 2025 23:12:30 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Thu, 23 Jan 2025 23:12:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3c572c5b651b10d04181f97ce4c0938b69ad43912e8c0bf19f77a4ea9a8f72e8`  
		Last Modified: Sun, 19 Jan 2025 13:02:58 GMT  
		Size: 199.1 MB (199054258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f917ac7a32bf48c832a0ba0c239739d2c45590c0b226f2c563e65acbc676c59c`  
		Last Modified: Thu, 23 Jan 2025 23:12:35 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb67ef85e47db4d2a778df2ad9372bb3d44717e804859ffaed503fbae55811f`  
		Last Modified: Thu, 23 Jan 2025 23:12:35 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8192936863631a5175ca6787b49593875c3eeaf6c27a2f30e70a6fadf91b12bb`  
		Last Modified: Thu, 23 Jan 2025 23:12:35 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e44fc286a5d790b0e1027e0f63930823879e7cdb9891f8097431a1480c85e93`  
		Last Modified: Thu, 23 Jan 2025 23:12:35 GMT  
		Size: 75.9 KB (75895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a2fb306b6b7f337040eb8aa771edf924263230401893c3da1d6ed5c660b0b60`  
		Last Modified: Thu, 23 Jan 2025 23:12:34 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d252c87bd13f23b6fd2458aec45bc2f1c7738dafd04e8c672d53af22cbcb5422`  
		Last Modified: Thu, 23 Jan 2025 23:12:34 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe25d95442b33bb386d49e678441b6b7eabb2d32b619f74df1f07d95ca336141`  
		Last Modified: Thu, 23 Jan 2025 23:12:45 GMT  
		Size: 208.5 MB (208489020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9efd5c606a068b39d4ea414f7220d93200cd07bdfe086b6262ffe4dddf430c7c`  
		Last Modified: Thu, 23 Jan 2025 23:12:34 GMT  
		Size: 104.0 KB (103997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd7607673a60f6efd7dd945944bb03d5b29d56c41ddb066e17369e50869f80b6`  
		Last Modified: Thu, 23 Jan 2025 23:12:34 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:24-ea-32-jdk-nanoserver` - windows version 10.0.20348.3091; amd64

```console
$ docker pull openjdk@sha256:9535bc132d436271893c0543a35fc4d96b68bb5074e29cfd75ef750bf6df74fb
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.3 MB (329339495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cd61edc757b9cbf4ed1e4133b0e5978649e0e1e35eb25c178dd88e62af1c09b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 12 Jan 2025 09:54:50 GMT
RUN Apply image 10.0.20348.3091
# Thu, 23 Jan 2025 23:08:16 GMT
SHELL [cmd /s /c]
# Thu, 23 Jan 2025 23:08:17 GMT
ENV JAVA_HOME=C:\openjdk-24
# Thu, 23 Jan 2025 23:08:18 GMT
USER ContainerAdministrator
# Thu, 23 Jan 2025 23:08:37 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Thu, 23 Jan 2025 23:08:38 GMT
USER ContainerUser
# Thu, 23 Jan 2025 23:08:38 GMT
ENV JAVA_VERSION=24-ea+32
# Thu, 23 Jan 2025 23:08:45 GMT
COPY dir:86d923ef445b254beb0a3a098fc78a6b4825f40d8c18f13f837cc4a7df771680 in C:\openjdk-24 
# Thu, 23 Jan 2025 23:08:52 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Thu, 23 Jan 2025 23:08:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fd3058b29fbd287119a2fa4d2d36a46fdee3bbada5fd9ef6f02f2d7d4cc143ab`  
		Last Modified: Tue, 14 Jan 2025 20:27:35 GMT  
		Size: 120.7 MB (120661554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:524c5ff1c502b3ce4bf67b204d5a5b77cbab15aebaedd40bad446fcaaa0f7216`  
		Last Modified: Thu, 23 Jan 2025 23:08:59 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72f6905910df7d14e3b583e3ffaa0f35a97451975c7ff48b55edef0a659d6f25`  
		Last Modified: Thu, 23 Jan 2025 23:08:58 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:954e0ab24a5e5cf838032468004a11aa5fe78bcaf9891961b0e49de3e8ddc8af`  
		Last Modified: Thu, 23 Jan 2025 23:08:58 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8b975cceb428afa88e15406457de104c5f407f32440ec45751fe5f9ef3d82d3`  
		Last Modified: Thu, 23 Jan 2025 23:08:58 GMT  
		Size: 85.4 KB (85410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8016125919e6a3858b84b207d85c9056c2c15e5d697a81e6bf57929b56a5d95e`  
		Last Modified: Thu, 23 Jan 2025 23:08:57 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4cc597579009d5fa55ccb3716d54f49ad5bbb2e1e9d22fecb6fd884ed145a7b`  
		Last Modified: Thu, 23 Jan 2025 23:08:56 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fedd76506ce74b04ef35498b93e2fce7c760db363e886d6598bf6a2cf4ef4f1b`  
		Last Modified: Thu, 23 Jan 2025 23:09:07 GMT  
		Size: 208.5 MB (208488746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367cb8ce6304f1b213c489fc6a5b05c27a481a1117a6810af61510536e49fdec`  
		Last Modified: Thu, 23 Jan 2025 23:08:57 GMT  
		Size: 97.6 KB (97562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134cfd3e2d5bd801fee21e9654bacebf7193d8a18e7a02995e9f9a092f2450ef`  
		Last Modified: Thu, 23 Jan 2025 23:08:57 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:24-ea-32-jdk-nanoserver` - windows version 10.0.17763.6775; amd64

```console
$ docker pull openjdk@sha256:9a994ed0a0c3d917ba2acae8711fc107b101ee1b50221bf74ee259b9a03c4b23
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.2 MB (368211611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c5344b4ecf411967ecad16234e5e752c34b145483cef6c9581d3eec11a60402`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Thu, 23 Jan 2025 23:08:34 GMT
SHELL [cmd /s /c]
# Thu, 23 Jan 2025 23:08:36 GMT
ENV JAVA_HOME=C:\openjdk-24
# Thu, 23 Jan 2025 23:08:36 GMT
USER ContainerAdministrator
# Thu, 23 Jan 2025 23:08:49 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Thu, 23 Jan 2025 23:08:49 GMT
USER ContainerUser
# Thu, 23 Jan 2025 23:08:50 GMT
ENV JAVA_VERSION=24-ea+32
# Thu, 23 Jan 2025 23:09:02 GMT
COPY dir:86d923ef445b254beb0a3a098fc78a6b4825f40d8c18f13f837cc4a7df771680 in C:\openjdk-24 
# Thu, 23 Jan 2025 23:09:08 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Thu, 23 Jan 2025 23:09:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Tue, 14 Jan 2025 20:45:12 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43a11d492babc456466e49db70691893af70094fce4d149e8d5bf2ef3139d81b`  
		Last Modified: Thu, 23 Jan 2025 23:09:13 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef6e76956e5a4dd35013202ee2ab433bc6b189195c47892aa1d80f3b249e965`  
		Last Modified: Thu, 23 Jan 2025 23:09:13 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c1664734d9b7983054a8f1b17bc021db9026effd3d02fcedf97e64d9e2747b5`  
		Last Modified: Thu, 23 Jan 2025 23:09:12 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2a1b683df1eb5a4f08686db506e2a57ec4c54367c9c20b7cf1bac9cb4a92004`  
		Last Modified: Thu, 23 Jan 2025 23:09:12 GMT  
		Size: 66.7 KB (66716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62cb45d0564755af2f5bfa0a3c287e1c6d87c5bb3f26ad8473b46ade25bfd912`  
		Last Modified: Thu, 23 Jan 2025 23:09:11 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef1deae82c8f9f2fd34a71d28fb8ccb27571e65358380b305b0bc385a96b81d1`  
		Last Modified: Thu, 23 Jan 2025 23:09:11 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ba9f04b4fb03757682bffbcb6ada1d507768f47224e375c5e54e9b30dca647`  
		Last Modified: Thu, 23 Jan 2025 23:09:23 GMT  
		Size: 208.5 MB (208488764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d186c6900bc0f7a7d5818a445b7de1a1a00c5e43a7217d4abc7700d0254ffa`  
		Last Modified: Thu, 23 Jan 2025 23:09:12 GMT  
		Size: 4.4 MB (4382323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d83dfacd4be28ea0a4de16d4db0a90aa88c41e0da0cc5eb0066227881928f1d5`  
		Last Modified: Thu, 23 Jan 2025 23:09:11 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
