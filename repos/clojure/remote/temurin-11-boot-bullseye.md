## `clojure:temurin-11-boot-bullseye`

```console
$ docker pull clojure@sha256:c9f3db38e73bf90d850a5e4fb05263efffe6ff0bd33f4a321bef3dcd60d559f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:9fb40d443f797380f218914ff2d1897add83d3949679c821680cb14c0712f18e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261544078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:924964d037e2bfb4448aee2d7e63282c680a883b4bc36b148ba747ab4a8ca9bd`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:11 GMT
ADD file:ff6bc341b5945acf6b9c190d70b5f5806fb3fae7b5c568ad6395aec1b95ba89c in / 
# Tue, 12 Mar 2024 01:21:11 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 06:12:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 28 Mar 2024 02:59:10 GMT
COPY dir:4cef005a87cd4606dd69ccb04c755a46f4aa2c925fb1aacc59928d64687208f2 in /opt/java/openjdk 
# Thu, 28 Mar 2024 02:59:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Mar 2024 02:59:11 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 28 Mar 2024 02:59:11 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 28 Mar 2024 02:59:11 GMT
WORKDIR /tmp
# Thu, 28 Mar 2024 02:59:18 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 28 Mar 2024 02:59:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 28 Mar 2024 02:59:18 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 28 Mar 2024 02:59:35 GMT
RUN boot
# Thu, 28 Mar 2024 02:59:35 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:ec335f17d0c74f7a270925cb1bbd29acc72ae904c6f4570f9ae369e3eebb64ed`  
		Last Modified: Tue, 12 Mar 2024 01:25:59 GMT  
		Size: 55.1 MB (55084969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda920a039665a5015c5cb162e10882e5997cc683456c339212c7aa546a6ebd7`  
		Last Modified: Thu, 28 Mar 2024 03:19:51 GMT  
		Size: 145.3 MB (145271223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c54824d6e2fb7cc76b32931bcace48b8fc98e5297228f311098f6e5b05fc23`  
		Last Modified: Thu, 28 Mar 2024 03:19:41 GMT  
		Size: 2.4 MB (2367301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe2abf346e900a8651f890e13a57cbe1c5b9e9a52976159084a06e2b4548a106`  
		Last Modified: Thu, 28 Mar 2024 03:19:44 GMT  
		Size: 58.8 MB (58820585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a8ef3ae67507d5d304496cdfff4c67c9d0be7ad06f037e2e54f8557f71ed652f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.9 MB (256911876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4f6a0490ea06528ad9b54559376d14408b7ff10bbd6d14407884963c69b157d`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:30 GMT
ADD file:6fedb173fe261ff0e13b004ca692b7edcc74dcc3c4384fee092b96ef9508992c in / 
# Wed, 10 Apr 2024 00:40:30 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:39:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 Apr 2024 04:44:19 GMT
COPY dir:d5fb8d9a38dea7496f2aff176bc9a34bbca80551c2dc57109d2dae5907a339ee in /opt/java/openjdk 
# Wed, 10 Apr 2024 04:44:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 04:44:23 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 10 Apr 2024 04:44:23 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 10 Apr 2024 04:44:23 GMT
WORKDIR /tmp
# Wed, 10 Apr 2024 04:44:27 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 10 Apr 2024 04:44:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 10 Apr 2024 04:44:28 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 10 Apr 2024 04:44:46 GMT
RUN boot
# Wed, 10 Apr 2024 04:44:47 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:197947a07d5f6c6ff020ca65dcea4e52671f85f67bee1b59af46cb0dc36580d9`  
		Last Modified: Wed, 10 Apr 2024 00:44:24 GMT  
		Size: 53.7 MB (53729176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b0f22ee6117e0db47b34d2db6b122dec65dbbf51b90af51d0ac68c526233be`  
		Last Modified: Wed, 10 Apr 2024 05:01:52 GMT  
		Size: 142.0 MB (142006323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8921dd8da6f5d05780956b95b7aee3d5884fbb815ff442210ac3bc4575c40c1e`  
		Last Modified: Wed, 10 Apr 2024 05:01:44 GMT  
		Size: 2.4 MB (2355777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcce96c742d3775f7a3790c99a2aedeaff40a7f21dc76e0badf3af014cd060c2`  
		Last Modified: Wed, 10 Apr 2024 05:01:46 GMT  
		Size: 58.8 MB (58820600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
