## `openjdk:25-ea-nanoserver-1809`

```console
$ docker pull openjdk@sha256:3f06200edcab2403a09711a3c74bf11da39fe7e3ab9080e3de6bc1ed26f4d64c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `openjdk:25-ea-nanoserver-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull openjdk@sha256:cb02345eafe0170e9bb89ce1a278d3b4c3746a5d06ab77d47dc2c96fd144c71b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.2 MB (367189530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c301ca3c447e4a136837329edb9d00d7f2aa9aae2968b8f65af21289b38eed04`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Fri, 31 Jan 2025 23:28:11 GMT
SHELL [cmd /s /c]
# Fri, 31 Jan 2025 23:28:13 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 31 Jan 2025 23:28:13 GMT
USER ContainerAdministrator
# Fri, 31 Jan 2025 23:28:26 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 31 Jan 2025 23:28:27 GMT
USER ContainerUser
# Fri, 31 Jan 2025 23:28:27 GMT
ENV JAVA_VERSION=25-ea+8
# Fri, 31 Jan 2025 23:28:38 GMT
COPY dir:0f89cb81afdb881ec0a835597e0e5b8ef37085da6c3213f99555c2a1da7025d9 in C:\openjdk-25 
# Fri, 31 Jan 2025 23:28:44 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 31 Jan 2025 23:28:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Tue, 14 Jan 2025 20:45:12 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d42c1ae81224c1ea7ce699b12d192d748b1ecf02e5126df393d7c70b58505a5`  
		Last Modified: Fri, 31 Jan 2025 23:28:50 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ecd80010e5ccd77287110d052a697b5befadb7c54d3bfb1bfddb91340fa299a`  
		Last Modified: Fri, 31 Jan 2025 23:28:49 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959db6ec01878f81bfb9d19996d458d8059d53371d87493c1dc5b14fa15d8889`  
		Last Modified: Fri, 31 Jan 2025 23:28:49 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68cfa1be79b42ef08999307e99bae955cdf605a9b0dab7232763ded67b4c6e11`  
		Last Modified: Fri, 31 Jan 2025 23:28:49 GMT  
		Size: 66.8 KB (66837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde0c8af2b9c7988bb47c659c44c29a2b8b496b27f10b96c19de3286b7eb16b2`  
		Last Modified: Fri, 31 Jan 2025 23:28:48 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b60a5307625f1899dfdfb1b3609a954d54d7a0552c9e0d4ae02106c4c60565`  
		Last Modified: Fri, 31 Jan 2025 23:28:48 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d141b506e164add6a8b2942ce00da282fa8f2895ba6b8fc23981f64f03b8057`  
		Last Modified: Fri, 31 Jan 2025 23:28:59 GMT  
		Size: 207.5 MB (207472832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d5da3c5e36167a92516f9e05d3daa10206d138fcf6e102f0b5031d09e7e5647`  
		Last Modified: Fri, 31 Jan 2025 23:28:48 GMT  
		Size: 4.4 MB (4375962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66cf3f419c9d9ef993600420f9a50b9d26fe704857a0ae32eb990a07f6aa98ad`  
		Last Modified: Fri, 31 Jan 2025 23:28:48 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
