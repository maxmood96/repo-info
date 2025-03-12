## `eclipse-temurin:21-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:039cdfcf164809ac45af3f35c37f3ce46229887739b4854c87c06a4e69349e89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3476; amd64

### `eclipse-temurin:21-jre-nanoserver-ltsc2025` - windows version 10.0.26100.3476; amd64

```console
$ docker pull eclipse-temurin@sha256:f54811764cb007e645beeae48786ef796de6b3287d1bcd724eb7e453370a4260
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.4 MB (255418943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b224e08709f0113b0bb85a448b8c55f10924053b0b04025b8b72fd9fb3fdccb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Mar 2025 05:48:38 GMT
RUN Apply image 10.0.26100.3476
# Wed, 12 Mar 2025 19:16:15 GMT
SHELL [cmd /s /c]
# Wed, 12 Mar 2025 19:16:16 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Wed, 12 Mar 2025 19:16:16 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 12 Mar 2025 19:16:17 GMT
USER ContainerAdministrator
# Wed, 12 Mar 2025 19:16:20 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Mar 2025 19:16:21 GMT
USER ContainerUser
# Wed, 12 Mar 2025 19:16:24 GMT
COPY dir:c0b7c132c85049081486a93cd76fe016c559b0b921796f63592a768b082ae9e2 in C:\openjdk-21 
# Wed, 12 Mar 2025 19:16:29 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:6008a43ec9274f69b461027b7f4e2fe6a71387d40072c0b5b4f0dbbfa688d8a5`  
		Last Modified: Wed, 12 Mar 2025 18:43:31 GMT  
		Size: 206.3 MB (206302205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3bd5935d46da96a5421c1d39f649744e8903f9c522e70f87f6298e14696e6f`  
		Last Modified: Wed, 12 Mar 2025 19:16:35 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02e5e396ae506e58c40a9d1251e3872e867516b0a26906b2f65412a2aed37a92`  
		Last Modified: Wed, 12 Mar 2025 19:16:35 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db3ba2c6b29e94a8d909d4deda2110e5e5482604fd0df6f8c19a775d946dbe59`  
		Last Modified: Wed, 12 Mar 2025 19:16:35 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27255a685465aa5ef906fb97907b61861d61b07067b9ecde68ae705a7110e87c`  
		Last Modified: Wed, 12 Mar 2025 19:16:33 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b9a6d18b218b0015651f877cd91e3c035894d5e42548cffe5985a8a11ddb354`  
		Last Modified: Wed, 12 Mar 2025 19:16:33 GMT  
		Size: 77.3 KB (77313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe1cab8786d2fbb86cfebdd8c586c618acd44fa2aba55879a240139cedebbf8f`  
		Last Modified: Wed, 12 Mar 2025 19:16:33 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:771954d370a7d5d7425e067636d1c55bac2acb86b73bfb324187d8752b9da3ef`  
		Last Modified: Wed, 12 Mar 2025 19:16:38 GMT  
		Size: 48.9 MB (48941037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:974c212bc38252e5fea9939e3f2adc25f7d2921ad04bdd2c8eb7766800b64d3e`  
		Last Modified: Wed, 12 Mar 2025 19:16:33 GMT  
		Size: 93.1 KB (93094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
