## `eclipse-temurin:8u422-b05-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:4f3db9a71ad8ac85c7dce1ecb7c2bea09eaac9bd6920573681eb6dad3014be8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2582; amd64
	-	windows version 10.0.17763.6054; amd64

### `eclipse-temurin:8u422-b05-jre-nanoserver` - windows version 10.0.20348.2582; amd64

```console
$ docker pull eclipse-temurin@sha256:5e11b1f72cca5866df5f34348dcd9b7f8afab120c2a2505b06dcf827bf765cbe
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160655969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eebbd0613928c686ff42e0bf847f58fd283eb9941eb8a278ed2edf08f512d9db`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 03 Jul 2024 09:30:07 GMT
RUN Apply image 10.0.20348.2582
# Wed, 10 Jul 2024 17:17:20 GMT
SHELL [cmd /s /c]
# Thu, 25 Jul 2024 17:25:11 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Thu, 25 Jul 2024 17:25:12 GMT
ENV JAVA_HOME=C:\openjdk-8
# Thu, 25 Jul 2024 17:25:13 GMT
USER ContainerAdministrator
# Thu, 25 Jul 2024 17:25:22 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 25 Jul 2024 17:25:22 GMT
USER ContainerUser
# Thu, 25 Jul 2024 17:26:08 GMT
COPY dir:9cd76711a1e21cd053ac2280c0520b18fc7c9ba73d3efc8192b2b62cbbddbbff in C:\openjdk-8 
# Thu, 25 Jul 2024 17:26:19 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:fdd0adf4702d813bb7fa724c9bf2343c201391c6d70a7a35135b18cc53499721`  
		Last Modified: Thu, 25 Jul 2024 17:31:42 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a94884a864d317b3caa2f721285e95de08018c4d1388ebfcc7b74d0b3371564c`  
		Last Modified: Thu, 25 Jul 2024 17:31:41 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4085421efae24344eed5fb063a3fed76207a5fa6434c58e5060c180b76b7821`  
		Last Modified: Thu, 25 Jul 2024 17:31:40 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f82df57eb258bb9e82243a6cda569545565c89aa9f4d19b7a9d443746926e680`  
		Last Modified: Thu, 25 Jul 2024 17:31:40 GMT  
		Size: 80.4 KB (80387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:183f1e530fbf61205e4a140565535007984ca4ba7ad524ccc77eca5b3a7d54d9`  
		Last Modified: Thu, 25 Jul 2024 17:31:40 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aeca43d3843d868cb322fbfe0a707c3dea0e24a6450c9017cf02367bd7ec672`  
		Last Modified: Thu, 25 Jul 2024 17:32:06 GMT  
		Size: 40.0 MB (40018511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f70d05893177c60583e6002fad80a813fc3bdb1cad17eacb716312fb8236c9`  
		Last Modified: Thu, 25 Jul 2024 17:32:01 GMT  
		Size: 60.9 KB (60914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8u422-b05-jre-nanoserver` - windows version 10.0.17763.6054; amd64

```console
$ docker pull eclipse-temurin@sha256:57bfa4722f988bc9eeb366ff4e600b694e72bbedf89b0cacbede6ce6c7fbf437
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.3 MB (195262339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e0f3a724741cc7109fce405b2bd9e16ed6aea5a496c766eea049304f58e590b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 03 Jul 2024 00:02:58 GMT
RUN Apply image 10.0.17763.6054
# Wed, 10 Jul 2024 16:38:43 GMT
SHELL [cmd /s /c]
# Thu, 25 Jul 2024 17:18:48 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Thu, 25 Jul 2024 17:18:48 GMT
ENV JAVA_HOME=C:\openjdk-8
# Thu, 25 Jul 2024 17:18:49 GMT
USER ContainerAdministrator
# Thu, 25 Jul 2024 17:18:55 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 25 Jul 2024 17:18:56 GMT
USER ContainerUser
# Thu, 25 Jul 2024 17:22:28 GMT
COPY dir:9cd76711a1e21cd053ac2280c0520b18fc7c9ba73d3efc8192b2b62cbbddbbff in C:\openjdk-8 
# Thu, 25 Jul 2024 17:22:38 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:848e7677215baaa1434649f02f2e139006fe6a40682b242095f66c53026b6c45`  
		Last Modified: Thu, 25 Jul 2024 17:30:20 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49149340728b0e7f5b7f7808d620efa8d5915f34b567ccdfea2e5660c32bd101`  
		Last Modified: Thu, 25 Jul 2024 17:30:19 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1578cbd6d39d4b23817f2fa5cb7e6271d3186bd15660e9534c1b74d53ac0db4`  
		Last Modified: Thu, 25 Jul 2024 17:30:17 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb2abf155b203af9595a7cadd2a3a3e6ff6134100de207677d10db7ef3b0ccd`  
		Last Modified: Thu, 25 Jul 2024 17:30:17 GMT  
		Size: 69.0 KB (68980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8f76482775d497e229394b5d2b7349baeeb1a2c81c9a8eab72a3e42fe6505d9`  
		Last Modified: Thu, 25 Jul 2024 17:30:17 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8916c30a2ce0fc2fe906d66c0fc2497a7696553412028003395570be97d49c`  
		Last Modified: Thu, 25 Jul 2024 17:31:15 GMT  
		Size: 40.0 MB (40018830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb82ba4184a22704313a33263c9219404217fc06ba10801b65f17434a590fa24`  
		Last Modified: Thu, 25 Jul 2024 17:31:10 GMT  
		Size: 87.5 KB (87452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
