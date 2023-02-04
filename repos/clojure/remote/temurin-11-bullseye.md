## `clojure:temurin-11-bullseye`

```console
$ docker pull clojure@sha256:d7de46708fdb58be2a637fd4a882f7e5008604be0a9bb20103c400ed84187ee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:d2d39ee0018054e6b4679812f0144e89570aea4b04d168d4b5d56c93882de7cb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.4 MB (325369287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06c5d730f05d66971b460fbcdeca10e80adb9667373bcc4654c93fd8754cbfc4`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 04 Feb 2023 06:51:26 GMT
ADD file:cc6a56676703ec7ab5db8f2f7bc18a3169c0816d38703845b6b77ae5342ab41c in / 
# Sat, 04 Feb 2023 06:51:27 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 14:05:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 04 Feb 2023 14:08:30 GMT
COPY dir:fdbc5e9dec2946fa124877176e92a68dd3fe3a70def5bb906a6040c4a1303a2d in /opt/java/openjdk 
# Sat, 04 Feb 2023 14:08:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Feb 2023 14:10:34 GMT
ENV CLOJURE_VERSION=1.11.1.1208
# Sat, 04 Feb 2023 14:10:34 GMT
WORKDIR /tmp
# Sat, 04 Feb 2023 14:10:51 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "4a3b1200c4d633202648dc3db6ed0a1311e75cc4baeee8fce32208c1eaa07537 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Sat, 04 Feb 2023 14:10:52 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Sat, 04 Feb 2023 14:10:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:699c8a97647f5789e5850bcf1a3d5afe9730edb654e1ae0714d5bd198a67a3ed`  
		Last Modified: Sat, 04 Feb 2023 06:55:53 GMT  
		Size: 55.0 MB (55025312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f565856b829993d14340c31a3780b450c70735c0b120d09f383ea8f7d156617`  
		Last Modified: Sat, 04 Feb 2023 14:21:45 GMT  
		Size: 198.5 MB (198475546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3efe3ef7765005124fee4f5f6c3ee8cc32d698aa2edfc040051f28ad8de0f12`  
		Last Modified: Sat, 04 Feb 2023 14:22:49 GMT  
		Size: 71.9 MB (71867811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1de5eeddc7d5ac55ddbfeb9551ee16dc0241ea4ae8fb0d43308b86e9acd7d45`  
		Last Modified: Sat, 04 Feb 2023 14:22:41 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:78ca27346d2dacfc3bbf46e7f14fa4398791ef6f85ed68bb5ef62f6208ba2ba3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.9 MB (320907024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc70a0579a78ec6b052c08671ee614833b57c9987e2c1b4655e16b833fe0dc30`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:26 GMT
ADD file:c5a7c65d67685092faa3456c1a772550aa6d06ac07e1f98a95d39c31e304dbf8 in / 
# Sat, 04 Feb 2023 06:17:27 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 17:02:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 04 Feb 2023 17:05:15 GMT
COPY dir:b661686bf8d434588756c45f2ef6e7f314f32f753cf180ef8fb45397388f098c in /opt/java/openjdk 
# Sat, 04 Feb 2023 17:05:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Feb 2023 17:07:02 GMT
ENV CLOJURE_VERSION=1.11.1.1208
# Sat, 04 Feb 2023 17:07:02 GMT
WORKDIR /tmp
# Sat, 04 Feb 2023 17:07:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "4a3b1200c4d633202648dc3db6ed0a1311e75cc4baeee8fce32208c1eaa07537 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Sat, 04 Feb 2023 17:07:17 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Sat, 04 Feb 2023 17:07:17 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:fac7262b6510529638951e16807cf1758f42c892ed924e334c27bb8bbcf7d7c2`  
		Last Modified: Sat, 04 Feb 2023 06:21:01 GMT  
		Size: 53.7 MB (53681927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf390961218a64e5f08d8723e6ac559e53df82459981dd9ae968a11a901c3d63`  
		Last Modified: Sat, 04 Feb 2023 17:16:51 GMT  
		Size: 195.2 MB (195240318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ae7eb3fa87b0635cc597ef5b8d95d07990939940dd0452a7fa7263e2364aea`  
		Last Modified: Sat, 04 Feb 2023 17:17:41 GMT  
		Size: 72.0 MB (71984162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6cbca92cae689a516de91d491a98b2b311eb8e988fd54d3cd6c5417f8994cb1`  
		Last Modified: Sat, 04 Feb 2023 17:17:34 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
