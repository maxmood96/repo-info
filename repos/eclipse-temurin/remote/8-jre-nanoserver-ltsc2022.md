## `eclipse-temurin:8-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:881a181ee2678225bf2dc936b7196d0f78b353f154c5d2f4adeb8fdc253c5531
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2700; amd64

### `eclipse-temurin:8-jre-nanoserver-ltsc2022` - windows version 10.0.20348.2700; amd64

```console
$ docker pull eclipse-temurin@sha256:61436c776536e7a4a61a499771144a02b10073418f3e90a6f28fffc435cccc56
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160674819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2f53b06a3cf596ad8f11bcbf09df1899d2665f194d099eac670ac1613572aac`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Sep 2024 23:48:03 GMT
RUN Apply image 10.0.20348.2700
# Wed, 11 Sep 2024 01:05:47 GMT
SHELL [cmd /s /c]
# Wed, 11 Sep 2024 01:05:48 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Wed, 11 Sep 2024 01:05:49 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 11 Sep 2024 01:05:49 GMT
USER ContainerAdministrator
# Wed, 11 Sep 2024 01:06:00 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 11 Sep 2024 01:06:01 GMT
USER ContainerUser
# Wed, 11 Sep 2024 01:06:35 GMT
COPY dir:9cd76711a1e21cd053ac2280c0520b18fc7c9ba73d3efc8192b2b62cbbddbbff in C:\openjdk-8 
# Wed, 11 Sep 2024 01:06:45 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:a447243899be39b01c34fc7e1bcecb47ce42b14668876fdd121f8b5e2d4d4a86`  
		Last Modified: Tue, 10 Sep 2024 22:28:02 GMT  
		Size: 120.5 MB (120509521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015f530aeae2fa9f5c34641a19099e9949880479ad7319678bd0506ba1927a95`  
		Last Modified: Wed, 11 Sep 2024 01:33:11 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef21dd038c1a6c24bf77ad129528c82f4db5372ddc60d7995e7e00d371596c7b`  
		Last Modified: Wed, 11 Sep 2024 01:33:11 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d0e194644c9171125eb77ddd53d8e8ec733ef20766f72803cd7b1a0ed866b17`  
		Last Modified: Wed, 11 Sep 2024 01:33:11 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20417130e443b6ddae87f09a182af4de4d2fc54934e7f37c5ff7593c632f32ac`  
		Last Modified: Wed, 11 Sep 2024 01:33:09 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ba644b18af11e2543cf583b6343beb7329f0d8c81d7bbb17d869e11bb7f364b`  
		Last Modified: Wed, 11 Sep 2024 01:33:09 GMT  
		Size: 79.5 KB (79477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4779375c8f2e097d1809a2d32a036d3e2c56431225c0eaa310afb7791eee429f`  
		Last Modified: Wed, 11 Sep 2024 01:33:09 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71c9ab06bd3ed14355c1d10387ecbe9a48c3f332173cf6061fa6813b6d820e9b`  
		Last Modified: Wed, 11 Sep 2024 01:33:45 GMT  
		Size: 40.0 MB (40018944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126cf4c834fd633ff0e17536fa16ede6e673e5c65290b1b44cb5866be3e9f998`  
		Last Modified: Wed, 11 Sep 2024 01:33:40 GMT  
		Size: 61.1 KB (61071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
