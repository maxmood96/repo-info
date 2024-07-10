## `eclipse-temurin:22-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:b40d4314271654677632f95caad551e35cdaeb0e51eef1f465ea31a397b3ab94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2582; amd64

### `eclipse-temurin:22-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.2582; amd64

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
