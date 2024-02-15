## `eclipse-temurin:17-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:02e7b299c9128f99761ca9c56b2081dc8191052e1230214e9f185edcdf3ae9ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `eclipse-temurin:17-jdk-nanoserver-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull eclipse-temurin@sha256:9d98f4ef0b6f68e3711061acdd11a262eff91c04ed00dbe811c8674d129b6f13
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.0 MB (295033094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66b17ed94d2dbfd918a7a3078738ffb998f74d4258b32b3a5f2c523e7fcaa573`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 04 Feb 2024 03:35:01 GMT
RUN Apply image 10.0.17763.5458
# Wed, 14 Feb 2024 19:41:52 GMT
SHELL [cmd /s /c]
# Wed, 14 Feb 2024 20:03:46 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 14 Feb 2024 20:03:46 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 14 Feb 2024 20:03:47 GMT
USER ContainerAdministrator
# Wed, 14 Feb 2024 20:03:56 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 14 Feb 2024 20:03:57 GMT
USER ContainerUser
# Wed, 14 Feb 2024 20:04:11 GMT
COPY dir:7333be24703ce46ff700c9b5bb2dfb5bd5b8a7a43d54ae48c80af36d6e10746c in C:\openjdk-17 
# Wed, 14 Feb 2024 20:04:24 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 14 Feb 2024 20:04:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:81be0bec766f944241448cd25317f59edcb12514e41b43288302e3e88d5462ad`  
		Last Modified: Tue, 13 Feb 2024 20:17:19 GMT  
		Size: 104.6 MB (104621606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cddfc54d18bb5861232283d3ff2ca5e214ade28a46dfcf6c1e7c7243809e5e85`  
		Last Modified: Thu, 15 Feb 2024 00:06:58 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffb981ab65987900b48adc21ebe2949755608c955366232d0ffc90279f30732e`  
		Last Modified: Thu, 15 Feb 2024 00:12:19 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750d966fd822c3283c05b8f1fe58a8480a5772c74a2eb20db24b36774b6d5c8c`  
		Last Modified: Thu, 15 Feb 2024 00:12:18 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13afa855e9d156e19c5588c5a8cddabf455899c0ebfed79ecadb12baef02113`  
		Last Modified: Thu, 15 Feb 2024 00:12:18 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce6b792723bfcdd26c27613c1c3457d72b7363761baf5e9d175085a1d256bc6d`  
		Last Modified: Thu, 15 Feb 2024 00:12:17 GMT  
		Size: 68.8 KB (68840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014f996fd63e6d2994ffce9350fa091ddda88161d528eec6e25ef2cd667cdc27`  
		Last Modified: Thu, 15 Feb 2024 00:12:17 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a4605dd0b2c78124b46dc978d5bf2edd0ef0b3769fba7b343e6d3cd80cbb4a0`  
		Last Modified: Thu, 15 Feb 2024 00:12:34 GMT  
		Size: 186.7 MB (186730766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b8b98fd10945068b367312fcaecdda9bde4260a6aaf56fda8ab96bd9b37f47`  
		Last Modified: Thu, 15 Feb 2024 00:12:18 GMT  
		Size: 3.6 MB (3604889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715df9aa488c348a8e0be88acbe206c9de0d29b5118bec8816d13de069677bde`  
		Last Modified: Thu, 15 Feb 2024 00:12:16 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
