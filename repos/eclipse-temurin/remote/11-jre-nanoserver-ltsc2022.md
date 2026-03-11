## `eclipse-temurin:11-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:c041e8ec41eb21ad68d9b3bd89ee232025d8464d7ec4b0da2985aa4cbac5772b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `eclipse-temurin:11-jre-nanoserver-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull eclipse-temurin@sha256:be9f9c4a4bed99fb007b1771253084dde178d92f483f0ac11875d8d4d14f741d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170552764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce6c1bac219021924d9a4b5db6e3c6ab1199c13a9b5712221ca2e60619dbe53e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Tue, 10 Mar 2026 22:36:30 GMT
SHELL [cmd /s /c]
# Tue, 10 Mar 2026 22:36:31 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Tue, 10 Mar 2026 22:36:31 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 10 Mar 2026 22:36:32 GMT
USER ContainerAdministrator
# Tue, 10 Mar 2026 22:36:34 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 10 Mar 2026 22:36:34 GMT
USER ContainerUser
# Tue, 10 Mar 2026 22:36:46 GMT
COPY dir:9d7273a61bdbfae69a7bd32ee7f3a7621be43375d7aad513ad72640646f9a6e0 in C:\openjdk-11 
# Tue, 10 Mar 2026 22:36:49 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3193fa96cb5f59168e86269680a94e06b22fe26237dbd8daa994296244ce8a`  
		Last Modified: Tue, 10 Mar 2026 22:36:54 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05a2a1789757f44a3ff8265c6faca3ec3c00491016a6b45c3f589abdc42e3f5`  
		Last Modified: Tue, 10 Mar 2026 22:36:54 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1f5912f13a69c1d979b9de5c9fd373442b91a2bb7a95a276d5c664a1f50292`  
		Last Modified: Tue, 10 Mar 2026 22:36:54 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e8c3de21fb069c0d9a64b22f43506f2a84454965fa9167529daf0d25d3204bf`  
		Last Modified: Tue, 10 Mar 2026 22:36:53 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b3a2302c672666326996672fc3ee42518fcb9decad36ee0c9ff0e0a7f8abab3`  
		Last Modified: Tue, 10 Mar 2026 22:36:53 GMT  
		Size: 77.8 KB (77752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ac8bcad787cffdbbbc8f63517360440afa9690d2fd5474269dbd6e5299721c`  
		Last Modified: Tue, 10 Mar 2026 22:36:53 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cbb5ade06b145d9379cb7dc7a599d1c0c432fc9856d45c9a517d7ffff6b0914`  
		Last Modified: Tue, 10 Mar 2026 22:36:58 GMT  
		Size: 43.7 MB (43718987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21bdeb9608dd47e6bfcae2a6f5b57bb8863295b28a2fc230bc648a59ba392518`  
		Last Modified: Tue, 10 Mar 2026 22:36:53 GMT  
		Size: 100.2 KB (100185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
