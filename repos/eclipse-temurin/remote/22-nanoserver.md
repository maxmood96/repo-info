## `eclipse-temurin:22-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:8dce503eabb40eac906508f2e9fb70708cb9331f5ce2d27f77687672a3d06ff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2582; amd64
	-	windows version 10.0.17763.6054; amd64

### `eclipse-temurin:22-nanoserver` - windows version 10.0.20348.2582; amd64

```console
$ docker pull eclipse-temurin@sha256:fd8c999cca8ef75def9eba6961ff7df0d4316019c3a8b43ded0de335d4dfc20e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.7 MB (320704463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:581c35277de96e628713ddc42b24f5786c5c4873d05ab9a164822d1e3d855e22`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 03 Jul 2024 09:30:07 GMT
RUN Apply image 10.0.20348.2582
# Wed, 10 Jul 2024 17:17:20 GMT
SHELL [cmd /s /c]
# Wed, 10 Jul 2024 17:21:50 GMT
ENV JAVA_VERSION=jdk-22.0.1+8
# Wed, 10 Jul 2024 17:21:51 GMT
ENV JAVA_HOME=C:\openjdk-22
# Wed, 10 Jul 2024 17:21:51 GMT
USER ContainerAdministrator
# Wed, 10 Jul 2024 17:21:58 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Jul 2024 17:21:59 GMT
USER ContainerUser
# Wed, 10 Jul 2024 17:22:10 GMT
COPY dir:b848142647370c7b57f8798114952350d05bf467cc96eb22cf5219409c8a4580 in C:\openjdk-22 
# Wed, 10 Jul 2024 17:22:22 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 10 Jul 2024 17:22:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:652774a5d82a114642848f8b0b8d486ec1b4995f9dda56e36fe4ac7563429990`  
		Last Modified: Tue, 09 Jul 2024 20:33:26 GMT  
		Size: 120.5 MB (120490378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1dbb650483c31087741ccfe7cfef17abfd7465711d0851e35d39eabc775bdae`  
		Last Modified: Wed, 10 Jul 2024 17:38:52 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a08ebf20fbe904b84fea17e450108b04546896985e66db0d560ed3313a33ebb2`  
		Last Modified: Wed, 10 Jul 2024 17:41:33 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:416088ac1d697c0b4e658ce2dc30fdb21af64e3c84979f927e4c93ec98aa3e58`  
		Last Modified: Wed, 10 Jul 2024 17:41:33 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d141c04cb4411ecd998a1e5987f3efcbc8f04e8edc0d86ce30687782ba331f2f`  
		Last Modified: Wed, 10 Jul 2024 17:41:33 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:347c73ff61d51debebd0828530e77ae4ff83fbfeea37af628df6e09098f8f534`  
		Last Modified: Wed, 10 Jul 2024 17:41:31 GMT  
		Size: 78.1 KB (78123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d9ca92578119f567c5c41ba7fd0597e7306029a54a67fadb807eb7469e9b6b`  
		Last Modified: Wed, 10 Jul 2024 17:41:31 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe2df582b3665aa5be5d08831e4f77883f6adff126ae167f7b4ec2917220842`  
		Last Modified: Wed, 10 Jul 2024 17:41:46 GMT  
		Size: 200.1 MB (200055582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be6be56bd817eb1b7b24d72ca5f9d9662d894f380348d0bca1fe9b6e92ad5965`  
		Last Modified: Wed, 10 Jul 2024 17:41:31 GMT  
		Size: 73.5 KB (73545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9224f529ada135db0a0042ff857447a24b5d4e45133ddc45319a9338d792a1d3`  
		Last Modified: Wed, 10 Jul 2024 17:41:31 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:22-nanoserver` - windows version 10.0.17763.6054; amd64

```console
$ docker pull eclipse-temurin@sha256:02af1034bc661877a313d05773a4c22ad721abe3f4dee5132db588d8a3352e1c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.0 MB (359049544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:271d01dd516fa247cf1c40b70eddd115f2b81e10c64b01e7df5c3fda377d6b3a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 03 Jul 2024 00:02:58 GMT
RUN Apply image 10.0.17763.6054
# Wed, 10 Jul 2024 16:38:43 GMT
SHELL [cmd /s /c]
# Wed, 10 Jul 2024 17:12:43 GMT
ENV JAVA_VERSION=jdk-22.0.1+8
# Wed, 10 Jul 2024 17:12:44 GMT
ENV JAVA_HOME=C:\openjdk-22
# Wed, 10 Jul 2024 17:12:45 GMT
USER ContainerAdministrator
# Wed, 10 Jul 2024 17:12:52 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Jul 2024 17:12:52 GMT
USER ContainerUser
# Wed, 10 Jul 2024 17:13:05 GMT
COPY dir:b848142647370c7b57f8798114952350d05bf467cc96eb22cf5219409c8a4580 in C:\openjdk-22 
# Wed, 10 Jul 2024 17:13:18 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 10 Jul 2024 17:13:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:53308e1345e8a502fe824770c132f9d645d42108fee87a0708ea8814c901e40d`  
		Last Modified: Tue, 09 Jul 2024 17:42:24 GMT  
		Size: 155.1 MB (155081383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c00a79547db1bc3ab4a5550f2ec9ba165e302f4a4984af3c1bfbbbe1726a3bf6`  
		Last Modified: Wed, 10 Jul 2024 17:28:00 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267a93688093f80ca8dad6f6eee6a284f8b5cc9d9513f090ffa870b2e76ee406`  
		Last Modified: Wed, 10 Jul 2024 17:37:34 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8513278cb5f417bcdd9bd49c4201bbe5858b11ff5e9dbc5813ca94e05cd84370`  
		Last Modified: Wed, 10 Jul 2024 17:37:34 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0957646dc3ce5ff5b9bab0b4ee6f9fca3d8e02e59851c100f30dad72ed7dc7`  
		Last Modified: Wed, 10 Jul 2024 17:37:34 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a82a3bfac767fb92f27a365bbdaf517aa0abe5a47399225fbb263332cdca67a`  
		Last Modified: Wed, 10 Jul 2024 17:37:32 GMT  
		Size: 69.5 KB (69480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c5d402c03451a70f00fdd335f9e0fa44e4b669193e85452132172681d8d5fa`  
		Last Modified: Wed, 10 Jul 2024 17:37:32 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d1ca3c2b7c8b7b783e0cc75d843668168826cd1420f28c8b052c89d08067756`  
		Last Modified: Wed, 10 Jul 2024 17:37:49 GMT  
		Size: 200.0 MB (200044535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3131968e8d7a1cdb06fa1bd953a283ceb0eee8e38999bcba8569dcbaf4dae42`  
		Last Modified: Wed, 10 Jul 2024 17:37:33 GMT  
		Size: 3.8 MB (3847177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e15907e58d89e912569353645a80f01e5113ed23094944920ce7dabc3d2ea7d8`  
		Last Modified: Wed, 10 Jul 2024 17:37:32 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
