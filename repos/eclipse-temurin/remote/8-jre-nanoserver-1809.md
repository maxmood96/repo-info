## `eclipse-temurin:8-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:254467fa6a8b431684505117e6921a45063b68f997cbfcaa413a990689d546c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `eclipse-temurin:8-jre-nanoserver-1809` - windows version 10.0.17763.6054; amd64

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
