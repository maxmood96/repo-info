## `eclipse-temurin:11-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:4b912d32a8d0c46a91c94ad01d857d6bc0c903fcca2620a197f0113043cb8e38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6905; amd64
	-	windows version 10.0.20348.4297; amd64

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.26100.6905; amd64

```console
$ docker pull eclipse-temurin@sha256:c0a7e3ca65dc8169d6875f861e209474d22eefef9f937459eda5bbae67e61293
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.9 MB (237875288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a71ea30d07de9e48039b2199c6834358a94382609562ce874534cbaae132ec36`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 22 Oct 2025 07:22:01 GMT
RUN Apply image 10.0.26100.6905
# Fri, 24 Oct 2025 19:21:07 GMT
SHELL [cmd /s /c]
# Fri, 24 Oct 2025 19:21:07 GMT
ENV JAVA_VERSION=jdk-11.0.28+6
# Fri, 24 Oct 2025 19:21:08 GMT
ENV JAVA_HOME=C:\openjdk-11
# Fri, 24 Oct 2025 19:21:08 GMT
USER ContainerAdministrator
# Fri, 24 Oct 2025 19:21:14 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 24 Oct 2025 19:21:14 GMT
USER ContainerUser
# Fri, 24 Oct 2025 19:21:19 GMT
COPY dir:58dfc6149e1020fd4be2dce5848817d79ad79993fb8b5211b36f6f0e332ab65c in C:\openjdk-11 
# Fri, 24 Oct 2025 19:21:23 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:9188956580c47f583c927f17e42f8825823890544237141f21ca4ef10ea55e60`  
		Last Modified: Fri, 24 Oct 2025 11:13:56 GMT  
		Size: 194.0 MB (194029378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:673c6d9ce2e6e261c72947f89344f156a194d4ecd461a5ac204760d341effc60`  
		Last Modified: Fri, 24 Oct 2025 19:22:22 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538092dfb002b37c5032c6c697b0cbc1eb48f2961f9bacf67ad705bcfaf79709`  
		Last Modified: Fri, 24 Oct 2025 19:22:22 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b63a8964786a07267869bc9519a5825249e3529ab844aaa4423fbc1a8e4ed7`  
		Last Modified: Fri, 24 Oct 2025 19:22:22 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4639c2dfc00648ac77be8dcad65ef91ada8d4d03b8ddddc9b56f839b39a56a23`  
		Last Modified: Fri, 24 Oct 2025 19:22:22 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff78301a9249cda7a1e4394fa67320b18535827565592e65f499d74495fd9a9`  
		Last Modified: Fri, 24 Oct 2025 19:22:22 GMT  
		Size: 70.6 KB (70643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ee5e2366c0210ef99769606387994598f4ab63db55f915751caf1157d6efef`  
		Last Modified: Fri, 24 Oct 2025 19:22:22 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6568cba713356b10562c6a8fb9dc38c66b49a5a9b4b339722254835c76ea6a11`  
		Last Modified: Fri, 24 Oct 2025 19:22:28 GMT  
		Size: 43.7 MB (43666628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf9f48d3fd31ad04a30bd90d62fdafc6a6bec22ba61df6071846541fc1eb306`  
		Last Modified: Fri, 24 Oct 2025 19:22:22 GMT  
		Size: 103.2 KB (103196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.20348.4297; amd64

```console
$ docker pull eclipse-temurin@sha256:15be9b86b6b4e68fc993f6c339492a049b5b4cc159a7994df290d50fb138fe5e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.5 MB (166526798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8806cfaa676cdda7c2ab628214099c3061521e3128674aa7afdbdab5e6ef276e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 22 Oct 2025 21:38:30 GMT
RUN Apply image 10.0.20348.4297
# Fri, 24 Oct 2025 19:21:14 GMT
SHELL [cmd /s /c]
# Fri, 24 Oct 2025 19:21:15 GMT
ENV JAVA_VERSION=jdk-11.0.28+6
# Fri, 24 Oct 2025 19:21:16 GMT
ENV JAVA_HOME=C:\openjdk-11
# Fri, 24 Oct 2025 19:21:16 GMT
USER ContainerAdministrator
# Fri, 24 Oct 2025 19:21:23 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 24 Oct 2025 19:21:24 GMT
USER ContainerUser
# Fri, 24 Oct 2025 19:21:41 GMT
COPY dir:58dfc6149e1020fd4be2dce5848817d79ad79993fb8b5211b36f6f0e332ab65c in C:\openjdk-11 
# Fri, 24 Oct 2025 19:21:45 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:2ac1abee018ad49a2f67a19d7f82901aac546affca76c86382db1a855dfcdaa1`  
		Last Modified: Fri, 24 Oct 2025 03:12:47 GMT  
		Size: 122.7 MB (122684063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9adff1d5bd5f0331cd06d179e8f7838493a03ac53a23db6febaf0765bbfe2607`  
		Last Modified: Fri, 24 Oct 2025 19:22:34 GMT  
		Size: 1.1 KB (1084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:717432d75b84b6bfa578121750325278fbe6b129941e66a6e065f383767a3757`  
		Last Modified: Fri, 24 Oct 2025 19:22:34 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978602495b44944aff3f3201ffe16d9fa46515aa4df08bb85cc89b8660e413e0`  
		Last Modified: Fri, 24 Oct 2025 19:22:34 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7aba60bd767ce7564f796ebfe7c90606c97943c7cd2529c3fb999fe31a49518`  
		Last Modified: Fri, 24 Oct 2025 19:22:34 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8372550b26d1ce804995503b50f3e31f861374fdd1443d565d72dbb46e4913dd`  
		Last Modified: Fri, 24 Oct 2025 19:22:34 GMT  
		Size: 73.6 KB (73586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325a06c1b4b123d558ccab4e38eae592a1681d208b02df5d26380c37d0b7e345`  
		Last Modified: Fri, 24 Oct 2025 19:22:34 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f81ae6d43af874d3d83268fb912b26596242e4eede619a0d1f8ea82f7cac47`  
		Last Modified: Fri, 24 Oct 2025 19:22:38 GMT  
		Size: 43.7 MB (43666230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea66c0d552e43174854ccde7390497007974087aaf1538976358fd016c406f1`  
		Last Modified: Fri, 24 Oct 2025 19:22:34 GMT  
		Size: 97.6 KB (97570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
