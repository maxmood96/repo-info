## `eclipse-temurin:11-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:608ab31c12a9ff7e2c20090e40fafd2fd471bb2383c7667c4b5c26d80b33d15e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `eclipse-temurin:11-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull eclipse-temurin@sha256:e9c7713328396e6b94c40e9dbfa06802ad863dd72383d05ccbfcedf2d37f86e0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.2 MB (321218565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2cbca55aaad35a0fc76c111597d61781df9e9e045902d31f27c938e91a11b11`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Tue, 11 Nov 2025 20:11:06 GMT
SHELL [cmd /s /c]
# Tue, 11 Nov 2025 20:11:07 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Tue, 11 Nov 2025 20:11:07 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 11 Nov 2025 20:11:07 GMT
USER ContainerAdministrator
# Tue, 11 Nov 2025 20:11:09 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 11 Nov 2025 20:11:09 GMT
USER ContainerUser
# Tue, 11 Nov 2025 20:11:16 GMT
COPY dir:207a50c3961430a3231a748eb9ce354eec00313f0753b2d5e8f279d3afd46cd8 in C:\openjdk-11 
# Tue, 11 Nov 2025 20:11:21 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 11 Nov 2025 20:11:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97be436214312a6298d6bd952225e6bd6e31ec3de7e85f7960b99f405d5e9ff8`  
		Last Modified: Tue, 11 Nov 2025 20:11:46 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2cba1572ea09f1a5ec91c52c80ca86a4329ddb251c6f1fa0177c423c2fb824e`  
		Last Modified: Tue, 11 Nov 2025 20:11:46 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4c427728add9669ee56c567aef50d673b57128e8be97db9f01c2e752f7b1822`  
		Last Modified: Tue, 11 Nov 2025 20:11:46 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06536cbc99cec4dc1adfba32f9011672f5e3e88fc0d18e47ed4616cabd9d3f7`  
		Last Modified: Tue, 11 Nov 2025 20:11:46 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996c77a0a9fc8d0b4e7eff97327c02a58bc14a9659dd79945116f586476430a5`  
		Last Modified: Tue, 11 Nov 2025 20:11:46 GMT  
		Size: 86.4 KB (86373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ed31a831be550aa176808e49bdaa111923d37fac52d2f7aa5e0884aeca7a6d`  
		Last Modified: Tue, 11 Nov 2025 20:11:46 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390e3592d980e3ea4f2ddb527a5be5442d465dce6b6121f76c7a502cbb0a28fc`  
		Last Modified: Tue, 11 Nov 2025 22:13:03 GMT  
		Size: 194.7 MB (194670240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b460cd67c65a9ed0b8b21f9966e413642b06ddfa37ad41d5de7c626844935d86`  
		Last Modified: Tue, 11 Nov 2025 20:11:46 GMT  
		Size: 106.5 KB (106516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c13a235935b4e5d4838ea160575ada0691aa6ff4e29e9080e11d46f127498fd6`  
		Last Modified: Tue, 11 Nov 2025 20:11:46 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
