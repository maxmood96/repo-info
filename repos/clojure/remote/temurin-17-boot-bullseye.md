## `clojure:temurin-17-boot-bullseye`

```console
$ docker pull clojure@sha256:07d464ee9ecc1645060c6df35508518f76f1f05b5a6e3b05a9e13df62607ecbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:537df2c17f6c13b61d5a635a5f8a55bee0cb89bc3a15e33b50d5e5d35a8a0005
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.1 MB (261139161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c50bd3a9d50f5c9d118ce082612be8f369cb4a50eb4af0d15dda1cd6a25ce82a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:29 GMT
ADD file:4fa73c8d113df02c8656b74ab87563432215332f3de78446a02e5ab7d6e2ab7a in / 
# Wed, 31 Jan 2024 22:35:29 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:44:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 31 Jan 2024 23:55:09 GMT
COPY dir:f32129cdf16cd5eee81dc24c5e5457011e489f134c2a5ee643ddf8ee33a43952 in /opt/java/openjdk 
# Wed, 31 Jan 2024 23:55:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Jan 2024 23:55:10 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 31 Jan 2024 23:55:10 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 31 Jan 2024 23:55:10 GMT
WORKDIR /tmp
# Wed, 31 Jan 2024 23:55:16 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 31 Jan 2024 23:55:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 31 Jan 2024 23:55:16 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 31 Jan 2024 23:55:35 GMT
RUN boot
# Wed, 31 Jan 2024 23:55:35 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 31 Jan 2024 23:55:35 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 31 Jan 2024 23:55:35 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7faaa42ac0c18c9baf539c97a5c8f042d02a77b05380cb57759e4407385710dc`  
		Last Modified: Wed, 31 Jan 2024 22:40:15 GMT  
		Size: 55.1 MB (55056963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a56f94c4ac8cf1517e75f20daa59713855b2a987cde3f5a473b73b8fca109c`  
		Last Modified: Thu, 01 Feb 2024 00:12:50 GMT  
		Size: 144.9 MB (144892488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4f4c3ff8947ca24726a619dac2b2aecc3370a14051399e92ddc42713524794`  
		Last Modified: Thu, 01 Feb 2024 00:12:39 GMT  
		Size: 2.4 MB (2368750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a794919da05b7033fdb34852494594c7bb3686cc938954ebdb2fb2aadb6b90c3`  
		Last Modified: Thu, 01 Feb 2024 00:12:41 GMT  
		Size: 58.8 MB (58820562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f11a7810235ef2bc7a1b438a7b1f5416edef7bcecba3ed91f9e250518a6f44`  
		Last Modified: Thu, 01 Feb 2024 00:12:38 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:86f97935fabe0f64d4b9d27d76867017fc7e856faada72097487cf589e3bf710
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.6 MB (258607594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b9dea87728c28ad0ffcfa6ba5b220a19c35f5c6ffa5520f58878013a1ce6df4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:33 GMT
ADD file:81cb49e646b9feb1ddeddea1cb6dbafa672a250f1553cc28eae09c955607236d in / 
# Wed, 31 Jan 2024 22:44:34 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:20:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Feb 2024 06:30:38 GMT
COPY dir:7c9e57a7678108e8f16bbe5ccb6616df59216fd52f6dd8321cc6163370ace185 in /opt/java/openjdk 
# Thu, 01 Feb 2024 06:30:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 06:30:41 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 01 Feb 2024 06:30:41 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 01 Feb 2024 06:30:41 GMT
WORKDIR /tmp
# Thu, 01 Feb 2024 06:30:46 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 01 Feb 2024 06:30:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 01 Feb 2024 06:30:46 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 01 Feb 2024 06:31:07 GMT
RUN boot
# Thu, 01 Feb 2024 06:31:07 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 01 Feb 2024 06:31:07 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 01 Feb 2024 06:31:07 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4b6eb2d0256d18652f84fd30c1db34ce9462e535a2d96fbf2f9044db000b13f5`  
		Last Modified: Wed, 31 Jan 2024 22:48:27 GMT  
		Size: 53.7 MB (53708267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f6d482f02e3b5ca72660a5fbf5cf406658f20ae04eec88846601f7517b97b36`  
		Last Modified: Thu, 01 Feb 2024 06:46:07 GMT  
		Size: 143.7 MB (143720894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe924a9196a80585a1487f0747f749f708c2f6faffdfe700976d73a8368c8153`  
		Last Modified: Thu, 01 Feb 2024 06:45:58 GMT  
		Size: 2.4 MB (2357384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb99c5fd85a62917ac56d700c52247d7947a09efa4d8198dfa203ab6162c43ba`  
		Last Modified: Thu, 01 Feb 2024 06:46:00 GMT  
		Size: 58.8 MB (58820650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c4b524c9a0adfcda3cca9ca7d902eb3e43bbb547f8e96e8a62138ab015626de`  
		Last Modified: Thu, 01 Feb 2024 06:45:57 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
