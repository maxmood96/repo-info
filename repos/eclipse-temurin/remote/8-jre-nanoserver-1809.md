## `eclipse-temurin:8-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:3c573362f318dd74fa296894f0de812fdb5ea9aa26e6418a659807b8c394e48a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `eclipse-temurin:8-jre-nanoserver-1809` - windows version 10.0.17763.6293; amd64

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
