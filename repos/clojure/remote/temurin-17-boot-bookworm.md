## `clojure:temurin-17-boot-bookworm`

```console
$ docker pull clojure@sha256:cec3d982461a0bbee474692d6529680756b976811ec4d5675df57914012857ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:9d0aa440386846558e280817d82809cfa68c9a846a49008ddd6bdfb132d85688
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.8 MB (258828326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc3ed9fbc464b1d93b1c88942c694af7942c6aced39cfb2c19edfe29f5795aa0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:05 GMT
ADD file:6d9e71f0d3afb0b288cf2c06425795d528a142872692072ab1cd1ad275b67d1f in / 
# Wed, 31 Jan 2024 22:35:06 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:41:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 17:18:01 GMT
COPY dir:2765b9c6732dde1d622a6314ea7119038a6031d832e1ec655de4889b7fd05a2e in /opt/java/openjdk 
# Fri, 02 Feb 2024 17:18:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 17:18:02 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 02 Feb 2024 17:18:02 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 02 Feb 2024 17:18:03 GMT
WORKDIR /tmp
# Fri, 02 Feb 2024 17:18:10 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 02 Feb 2024 17:18:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 02 Feb 2024 17:18:11 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 02 Feb 2024 17:18:30 GMT
RUN boot
# Fri, 02 Feb 2024 17:18:30 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Fri, 02 Feb 2024 17:18:31 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 02 Feb 2024 17:18:31 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6a299ae9cfd996c1149a699d36cdaa76fa332c8e9d66d6678fa9a231d9ead04c`  
		Last Modified: Wed, 31 Jan 2024 22:39:27 GMT  
		Size: 49.6 MB (49583754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e272de56020947d967cc38ae404bdf929ec35fa85009eb7fcaa4a05298c22e`  
		Last Modified: Fri, 02 Feb 2024 17:35:57 GMT  
		Size: 144.9 MB (144893230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5e0fb9d2243c09c53e49772bb638ef4c27d719b0101711262bbf1931f77de3`  
		Last Modified: Fri, 02 Feb 2024 17:35:46 GMT  
		Size: 5.5 MB (5530483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbe76830c55a0e20e23ccd54f1344609b0febcb8df79993b2807d36ab406c10`  
		Last Modified: Fri, 02 Feb 2024 17:35:48 GMT  
		Size: 58.8 MB (58820458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e299957787c28e72204fd5d5f3951f71d497ea2a4caa81b73080cf22253c8314`  
		Last Modified: Fri, 02 Feb 2024 17:35:45 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3f6d4b451f21a07bfb8dfe192f0eeb979772bd313bb4cf2224893cf4816bf77a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.5 MB (257510525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08abbb35a1f1827eb019c274df4a82f7817e3e7bc755102afcb766154d8255d6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:15 GMT
ADD file:8bc7f537dd3dc4b92ec9006080fd563cc79205ee1ec3f456d03e869125a5bc21 in / 
# Wed, 31 Jan 2024 22:44:15 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:18:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 08:27:01 GMT
COPY dir:1e33e1b9b4d5ff1fcafcf70a5b147d046ddd08f2a0ffd21b97536e3a6e636c5f in /opt/java/openjdk 
# Fri, 02 Feb 2024 08:27:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 08:27:05 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 02 Feb 2024 08:27:05 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 02 Feb 2024 08:27:05 GMT
WORKDIR /tmp
# Fri, 02 Feb 2024 08:27:11 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 02 Feb 2024 08:27:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 02 Feb 2024 08:27:11 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 02 Feb 2024 08:27:29 GMT
RUN boot
# Fri, 02 Feb 2024 08:27:29 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Fri, 02 Feb 2024 08:27:29 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 02 Feb 2024 08:27:29 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:66932e2b787d33a94ee3eb8b489be6e6838b29f5c1d732262da306da9b1f2eed`  
		Last Modified: Wed, 31 Jan 2024 22:47:40 GMT  
		Size: 49.6 MB (49615296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2123fb31cbd519f0e5acdcb92c2fd15e1872407955fb24a687b068c997bb7e12`  
		Last Modified: Fri, 02 Feb 2024 08:43:27 GMT  
		Size: 143.7 MB (143720880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f7d9c83bb4abc4f4787da33eb3ba7106fa905cbf4e695e9060e9f8b0b632ec`  
		Last Modified: Fri, 02 Feb 2024 08:42:23 GMT  
		Size: 5.4 MB (5353323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4ccfbf44a4a8c4acee71d8ffb89ec743b6b2fd73187912bf42fb3d3111b5e5`  
		Last Modified: Fri, 02 Feb 2024 08:42:27 GMT  
		Size: 58.8 MB (58820626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd7c65829822f5ed41ede73554098868b093a74fc7d4726ed181cb40f930099`  
		Last Modified: Fri, 02 Feb 2024 08:42:22 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
