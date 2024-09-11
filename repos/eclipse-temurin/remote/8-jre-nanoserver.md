## `eclipse-temurin:8-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:f141179b3e6cff5d6eab40a81e9f845b8ffb4434c4b0935354e3580c769e7dbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2700; amd64
	-	windows version 10.0.17763.6293; amd64

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.20348.2700; amd64

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

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.17763.6293; amd64

```console
$ docker pull eclipse-temurin@sha256:4bf33ec8f0308b493b85fb5f5c96970b9e05d311bd10ad28d113dcd7d0599bef
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.2 MB (195232762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c26874b65056aad211c2f80dc4159ab97b86d231a905d673872327972a6ed491`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Sep 2024 01:02:10 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 00:38:01 GMT
SHELL [cmd /s /c]
# Wed, 11 Sep 2024 00:38:02 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Wed, 11 Sep 2024 00:38:03 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 11 Sep 2024 00:38:03 GMT
USER ContainerAdministrator
# Wed, 11 Sep 2024 00:38:13 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 11 Sep 2024 00:38:14 GMT
USER ContainerUser
# Wed, 11 Sep 2024 00:40:59 GMT
COPY dir:9cd76711a1e21cd053ac2280c0520b18fc7c9ba73d3efc8192b2b62cbbddbbff in C:\openjdk-8 
# Wed, 11 Sep 2024 00:41:10 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:a8b325bcb6d89afa770bc0d80d724a7529f3c8bdf940ab5418ad8d6b94fb07f0`  
		Last Modified: Tue, 10 Sep 2024 17:40:58 GMT  
		Size: 155.1 MB (155080848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340318059288cbbdb326eea5b7079e789361251409038a37867d4e395c9404a5`  
		Last Modified: Wed, 11 Sep 2024 01:21:36 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02106b426902c7615863c4b56b01b06cc3d3b7fa8855c49224ee7699989fefba`  
		Last Modified: Wed, 11 Sep 2024 01:21:36 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c43928233a5d3038e98674df1be7f1f29e0801669f62acabaf0d113b33ee4e`  
		Last Modified: Wed, 11 Sep 2024 01:21:35 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95b418b25d7d864e6ccdad65299b0972dcbd0dde17c1f20f6b0e3d2dd7829bca`  
		Last Modified: Wed, 11 Sep 2024 01:21:33 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a59736e850920a7737b3a01e95f615c9dd3ef10af0fa911b2ec0285135734c4`  
		Last Modified: Wed, 11 Sep 2024 01:21:34 GMT  
		Size: 69.5 KB (69510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d38143bdbd943337ada11ffd205aacee07168442061f9d5b5cbdd9bb6c7de211`  
		Last Modified: Wed, 11 Sep 2024 01:21:34 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84150dfa9bf84eaf3721884ac3aaa8b20c5434e0fdf5ae06b70186e2d98f7a29`  
		Last Modified: Wed, 11 Sep 2024 01:22:45 GMT  
		Size: 40.0 MB (39994642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:359b03f950d3e410925f7704af1f7296dee7a986931130657765e5b3abd58393`  
		Last Modified: Wed, 11 Sep 2024 01:22:40 GMT  
		Size: 82.0 KB (82027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
