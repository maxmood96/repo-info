## `clojure:temurin-11-bullseye-slim`

```console
$ docker pull clojure@sha256:a8651229d9de27a5b636550c82a17d7d2386ad63962892620fb891b7f241f0ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b70753df6a78cc117424e54f24fff7ea23a0fa674fb7c076e716b32387884937
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234884078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa6ecda56846df24eb1805aaf06e390df9f20c778b9a423fa28e20ba0455e98`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c8e1eb8ab3b017bd9e33ddec83ebdd8292c542bbd14a8d5a6cfa2edc3ad3b8eb`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 30.3 MB (30254604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c383f0666f93eca3b75c433c19832872e702de8e0d9fed5f5e2a93475f2613`  
		Last Modified: Mon, 28 Apr 2025 22:07:03 GMT  
		Size: 145.6 MB (145635846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07f826d0d9eb0dffa35281ca19b8079a75dd0216a258568c1561e5af50439a8`  
		Last Modified: Mon, 28 Apr 2025 22:07:01 GMT  
		Size: 59.0 MB (58992985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c64535ac197f340a3e6f95bfc957ff8235e8afb24e1d4a905eb9a35a8931a9`  
		Last Modified: Mon, 28 Apr 2025 22:07:00 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:eac4a9d3e0971b6f1f86e06f094957c613060f30ad02f9eb50c3f75a23b7207f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5153518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b967a0ba80a1a82737c0f86e7f594b368605eec7b1aa626a834247d2b8666952`

```dockerfile
```

-	Layers:
	-	`sha256:ad2d5696c7112f455048241ece16a500b559828c4bd5698b9cd802f6f83a2b13`  
		Last Modified: Mon, 28 Apr 2025 22:07:00 GMT  
		Size: 5.1 MB (5139208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9c37e90974b8a39519fe612b71632fc307f29a8f10c54319e415cc706a01b2d`  
		Last Modified: Mon, 28 Apr 2025 22:06:59 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f60bd2e2595fd3315d495231d947786e4afaaa2189c666f5cc5660a560fc6176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.3 MB (230294690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:122ac25f0568bfec16af5e62fd9e31c84ce21b2d825df82e389d897d8e0dc006`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:5d3a81360c5bb9281a4f735a1468429a1898f1a4fc24a2581dde4cf28ace4488`  
		Last Modified: Mon, 28 Apr 2025 21:21:09 GMT  
		Size: 28.7 MB (28744645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e78d2c29016836785703fd1a3b6a2c3ab908b7865aa01b553d5dbdeee44eea`  
		Last Modified: Tue, 29 Apr 2025 20:16:23 GMT  
		Size: 142.4 MB (142422045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c024bd4682e386307bac70d0cbaf908925038381daca6ee0ee73779361718c`  
		Last Modified: Wed, 30 Apr 2025 01:09:36 GMT  
		Size: 59.1 MB (59127355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18c645d702f0221fb90415aa2ceaa9c8715dbfba84df04060e2f942a3a0f1917`  
		Last Modified: Wed, 30 Apr 2025 01:09:34 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:15db83609d28f20974c55c4090cc6b9a93cde20073bb07f5243ba21f19683b90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5159986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39694411ed6af6826b4fd1f189740c7af66dbbc4cc39acf47f101fe7c44670f9`

```dockerfile
```

-	Layers:
	-	`sha256:07e4530b5e45a1d51225ee659c50ae6b2df87fcefbca73f4531bfe55c6479f4e`  
		Last Modified: Wed, 30 Apr 2025 01:09:35 GMT  
		Size: 5.1 MB (5145558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7adbab649b282b63bf2eb38ae5a12107b0687ae2d9315d6ee3de045aee48755c`  
		Last Modified: Wed, 30 Apr 2025 01:09:34 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json
