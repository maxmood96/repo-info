## `clojure:temurin-24-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:8b5a63e8a100e76b49c8d610394884e561af18d4cbddb0ac995144cccce99e09
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:173935897772ab63959bc4b4f1697ac89314d71975360c228b2a5220adce39f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 MB (219434520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:386c7a4ba3342437f4b473a59bcea4deb8a88bc4e8ea7e37370ebd8c9d9c69c5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:23b7d26ef1d294256da0d70ce374277b9aab5ca683015073316005cb63d33849`  
		Last Modified: Tue, 08 Apr 2025 00:22:55 GMT  
		Size: 48.5 MB (48490541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c7be967748db1deb3f5da8beb1bb895286c6537627e1c7ba541382372ee761`  
		Last Modified: Tue, 08 Apr 2025 01:36:54 GMT  
		Size: 89.9 MB (89949049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3328a08b39171d34ce1e6338293a17e366855f4a86dcc007df6cb346be44a1bc`  
		Last Modified: Tue, 08 Apr 2025 01:36:55 GMT  
		Size: 81.0 MB (80993891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833ff02204b1d63538dfaed3593cb5a3d2c541ab041b44b9474516a617176328`  
		Last Modified: Tue, 08 Apr 2025 01:36:53 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3965fc47bee9a257f6e677ba9f5c4189d42749d9a5300b01e21c3221c9fa4c`  
		Last Modified: Tue, 08 Apr 2025 01:36:53 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:dc384af9b9d464c3ade7088217ea1ef32e1ff99b9436493627ea7874e70d2e15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7140290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75eba903d144609f3301838201f4577623c15e922a346eb27288c1d1233a0bab`

```dockerfile
```

-	Layers:
	-	`sha256:068f173d029d769f1d48f5cb2c5299656112efb973462dd8cc09cafd098af00f`  
		Last Modified: Tue, 08 Apr 2025 01:36:53 GMT  
		Size: 7.1 MB (7123792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a36b9fa102ff07aa2aba3e36b992f59553613fb57d34441057dab20787eed6c7`  
		Last Modified: Tue, 08 Apr 2025 01:36:53 GMT  
		Size: 16.5 KB (16498 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3638c6f30dafcab15f2ecc2f44eb928191e06cc4c73cf1b318295fbf48b205bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.2 MB (218241251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:516532cbe635038e7646092592631a56f7fb7843d0e36d0b726593549bd70e2f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:545aa82ec479fb0ff3a196141d43d14e5ab1bd1098048223bfd21e505b70581f`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.3 MB (48304855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32f1d4584a0aa49d6c0f2a0d382f28e60f4fc57ebb8548010197c1a8c2e0418`  
		Last Modified: Thu, 27 Mar 2025 17:53:16 GMT  
		Size: 89.1 MB (89092702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acbcbb2220cc29c57d15cf53ff89f0c4fb19dce9011fb91600590e71c0e0ddf2`  
		Last Modified: Thu, 27 Mar 2025 17:58:37 GMT  
		Size: 80.8 MB (80842652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa23cce58189077096bb9b63d2973bbd76034a26eb8cb037c3a0bf229e1abad8`  
		Last Modified: Thu, 27 Mar 2025 17:58:35 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d93a2f2f94595101b26c7c9a0f9d8afec2b5000969982883fe4ec1eb597e1d`  
		Last Modified: Thu, 27 Mar 2025 17:58:35 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:37bdd291ac808128e41c31b8b8b4e8419d9e0d07371ae3c3e22575fb5848ce9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7144847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f62fb81c059c87cc55e90bf896e5451cf40bba79815cfa833f5ac04940203840`

```dockerfile
```

-	Layers:
	-	`sha256:1c8153facf09c14d567ae289aa45aa8b9c8612d4f54d6f7755aa37e23d5a0f1a`  
		Last Modified: Thu, 27 Mar 2025 17:58:35 GMT  
		Size: 7.1 MB (7128208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efaefebea300d26c674f7394eee2698e687f1bd1e451ff62a1b0ba8aba7e7e8a`  
		Last Modified: Thu, 27 Mar 2025 17:58:35 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json
