## `eclipse-temurin:11-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:11420518eac49099f179bffbcdcf3552ca3e77d7ab1d11debfe0dbb05d7d0446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3194; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.26100.3194; amd64

```console
$ docker pull eclipse-temurin@sha256:2cf2d8d2b089fd554a031da431ca86ac192e82edafc31b2712548f02a2e5da03
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.7 MB (249709172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76cce98a0bf9348a8cdc6d57c6777c2ab6807fc3d8c902cddf833b44a898cce2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 08 Feb 2025 22:31:47 GMT
RUN Apply image 10.0.26100.3194
# Thu, 27 Feb 2025 19:13:10 GMT
SHELL [cmd /s /c]
# Thu, 27 Feb 2025 19:13:11 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Thu, 27 Feb 2025 19:13:11 GMT
ENV JAVA_HOME=C:\openjdk-11
# Thu, 27 Feb 2025 19:13:12 GMT
USER ContainerAdministrator
# Thu, 27 Feb 2025 19:13:15 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 27 Feb 2025 19:13:16 GMT
USER ContainerUser
# Thu, 27 Feb 2025 19:13:20 GMT
COPY dir:e7319a06d2b9171c954fc18de0614fa7d0eb408950b795be61492806db04a6ea in C:\openjdk-11 
# Thu, 27 Feb 2025 19:13:23 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:e075dd07cbf907b7da8dbd8365b73a71ac92a834b78f520bd976cb97e0fcc0a1`  
		Last Modified: Wed, 12 Feb 2025 22:34:59 GMT  
		Size: 205.9 MB (205890263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176975e7807608213dcfc7aaba56602d0bc384a4c2310aabec598c92a2ac13fc`  
		Last Modified: Thu, 27 Feb 2025 19:13:27 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14b3cdc1414c00dc455a902de8cc16c822ef26d712a82736b861b6106ed2861e`  
		Last Modified: Thu, 27 Feb 2025 19:13:27 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4babe52a938d08459b4bf861d43d92d7db4a99e1f46926373bd54a7a67bd180a`  
		Last Modified: Thu, 27 Feb 2025 19:13:27 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a2679c39a7e8ac37b53647a58e072988fcbb804c3fac27f9c2634ddee347a2`  
		Last Modified: Thu, 27 Feb 2025 19:13:26 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ffbd8347a38ccfaf13e1855e087f69601127b4e85b214cc96d764ff28fb1956`  
		Last Modified: Thu, 27 Feb 2025 19:13:26 GMT  
		Size: 73.4 KB (73369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce4d7854ed75542c1292acad2c37af912160a3fe07f455c0affad8344918a401`  
		Last Modified: Thu, 27 Feb 2025 19:13:26 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca6320c2ff76bace1470199635356b9abea145cf2946d6a551c0a90331105fd0`  
		Last Modified: Thu, 27 Feb 2025 19:13:30 GMT  
		Size: 43.7 MB (43656643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8273d39b6784796e9730a178ed76875ccc4998396c14e68c75bc223d9e0c4c35`  
		Last Modified: Thu, 27 Feb 2025 19:13:26 GMT  
		Size: 83.6 KB (83636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.20348.3207; amd64

```console
$ docker pull eclipse-temurin@sha256:b6a59ba7f660f503e3343ccd0ad0804529cdf26d8654a8e00e021dfb9941631f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.5 MB (164504583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2085b5ed99e6d5b8bffd378311981d871c7bfd296353d22700c62d6533c8b11`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Feb 2025 20:45:43 GMT
RUN Apply image 10.0.20348.3207
# Thu, 13 Feb 2025 01:16:29 GMT
SHELL [cmd /s /c]
# Thu, 13 Feb 2025 01:16:29 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Thu, 13 Feb 2025 01:16:30 GMT
ENV JAVA_HOME=C:\openjdk-11
# Thu, 13 Feb 2025 01:16:30 GMT
USER ContainerAdministrator
# Thu, 13 Feb 2025 01:16:32 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 13 Feb 2025 01:16:33 GMT
USER ContainerUser
# Thu, 13 Feb 2025 01:16:36 GMT
COPY dir:e7319a06d2b9171c954fc18de0614fa7d0eb408950b795be61492806db04a6ea in C:\openjdk-11 
# Thu, 13 Feb 2025 01:16:39 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:938e4585b186fc3df3c1959d47ba7a634fea121cec7545db7923ceb191d99a33`  
		Last Modified: Tue, 11 Feb 2025 22:43:09 GMT  
		Size: 120.7 MB (120666610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d84b9361672150f6122c04cf4fff6343213f665f38eda134a99af68c22b17926`  
		Last Modified: Thu, 13 Feb 2025 01:16:45 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fcdb7bf09d85ff6e864d840657d33158d189bb2af76374e2d0ec152e015a75d`  
		Last Modified: Thu, 13 Feb 2025 01:16:45 GMT  
		Size: 1.1 KB (1090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b8bee2434bc2eb9a7f63ad386fb11a140096c1591d1b73d6e1203a8bbeff054`  
		Last Modified: Thu, 13 Feb 2025 01:16:45 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf4264f641802aa08bcc626cc8ea055a10bac5d1e422c4f12de629719aa2b20`  
		Last Modified: Thu, 13 Feb 2025 01:16:43 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4163a1a3ebde03da75961cda9490f17acb20966630645765aed774799d85a10`  
		Last Modified: Thu, 13 Feb 2025 01:16:43 GMT  
		Size: 76.8 KB (76777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d46a99f0f09d0527640040aea0e6b380fdd5541605a556dce7a3c8ca28d4d5`  
		Last Modified: Thu, 13 Feb 2025 01:16:43 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbcce110fc393fa71dd45591b3e1869697276f26d43dd8fa17c5df1650b03f4d`  
		Last Modified: Thu, 13 Feb 2025 01:16:47 GMT  
		Size: 43.7 MB (43656316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd973ce35b75d796cfb04ab75e9b69e505b50ee80c4355f95718551bf318c8d4`  
		Last Modified: Thu, 13 Feb 2025 01:16:43 GMT  
		Size: 99.5 KB (99484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.17763.6893; amd64

```console
$ docker pull eclipse-temurin@sha256:c39ef3f488dd0e117b4d0f748d2adaead58aa71c6954adc657496beaabeb5d3b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.8 MB (150755012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:308fc37e08e57c0ccd423b78f877038df0ba1da028f99adae39be6fc3abeb35c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Feb 2025 17:59:14 GMT
RUN Apply image 10.0.17763.6893
# Thu, 13 Feb 2025 01:17:51 GMT
SHELL [cmd /s /c]
# Thu, 13 Feb 2025 01:17:54 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Thu, 13 Feb 2025 01:17:54 GMT
ENV JAVA_HOME=C:\openjdk-11
# Thu, 13 Feb 2025 01:17:55 GMT
USER ContainerAdministrator
# Thu, 13 Feb 2025 01:17:57 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 13 Feb 2025 01:17:58 GMT
USER ContainerUser
# Thu, 13 Feb 2025 01:18:02 GMT
COPY dir:e7319a06d2b9171c954fc18de0614fa7d0eb408950b795be61492806db04a6ea in C:\openjdk-11 
# Thu, 13 Feb 2025 01:18:06 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:5965f4f533e4b42b41b3fd8dff42c138329bf35311ce090d4c7cc4acd5a59360`  
		Last Modified: Tue, 11 Feb 2025 20:25:23 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095d2f8fedfb5490450bbd42c650ea5d879829b73d6f5ab128cb6b99cf7a1b1b`  
		Last Modified: Thu, 13 Feb 2025 01:18:10 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c324be8909439bb20e59510dcc1cfd6828b947742dc3f8cb5b9b0f8d0e7dfec6`  
		Last Modified: Thu, 13 Feb 2025 01:18:10 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba4fba56537ab4cead3ed14efb6626b92d834b17f25657611498eec9cbb1be9`  
		Last Modified: Thu, 13 Feb 2025 01:18:10 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2843275d9d9882ba668243c2482f8db3d51e7b1dde603ab7350605419a97d70`  
		Last Modified: Thu, 13 Feb 2025 01:18:09 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfea8d0be4f0432ad954c2318dfd13da35c0dbd442686eae5cbbe5c63c761057`  
		Last Modified: Thu, 13 Feb 2025 01:18:09 GMT  
		Size: 80.3 KB (80344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5fd1c113e43733acb1b85aac9f5b64a03a287d2d535f5c2ea37f7b642377258`  
		Last Modified: Thu, 13 Feb 2025 01:18:09 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b05bc421a8d6f292f7a0ba0b7fcf939e3a57ef074aaabec401f79f43225008`  
		Last Modified: Thu, 13 Feb 2025 01:18:14 GMT  
		Size: 43.7 MB (43656310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f496ad1d58b8222a977e8b349349a563ed33dd74d28f6853355fa9f02fd84f3`  
		Last Modified: Thu, 13 Feb 2025 01:18:09 GMT  
		Size: 97.5 KB (97493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
