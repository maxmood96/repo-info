## `clojure:temurin-11-tools-deps-1.12.1.1550-bullseye`

```console
$ docker pull clojure@sha256:8ad90b6a1057cd1b49cde1e5fa45743c7dd47006547929e69bd271a510157538
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.1.1550-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:4174acac1fc8bc43ba637e896a98cbdae4540463489017b156a991ceb19f2647
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.8 MB (268824008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aedb51430018f1f23bbfb5cb956ae97b4884379a4282bd5dbab7da7586d57e31`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:078965fc7cf303b72cc4eef5479dc2dbf5bc84fb8e6052a89b9b5362e14b3651`  
		Last Modified: Tue, 12 Aug 2025 20:44:43 GMT  
		Size: 53.8 MB (53755344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0deaa53fc4da5156f9b4a4182c75d78cb3c6cb72acae3bcee65262adaf4a77a`  
		Last Modified: Thu, 14 Aug 2025 02:22:47 GMT  
		Size: 145.7 MB (145658203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1ac6491c2749220d99c528b9489872834840c0cfe4ea8fe96e212c50338592c`  
		Last Modified: Tue, 12 Aug 2025 21:36:22 GMT  
		Size: 69.4 MB (69409820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e55a2cd0f421e142c2759480dbe96539f0e575b97ac58028c3fc78aa73e589`  
		Last Modified: Tue, 12 Aug 2025 21:36:09 GMT  
		Size: 609.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1550-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:d0c25dc159a65c8bdb26e7ca6d6f04a5f7a6da92f37d9cb022c270e1e3ddad22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7430031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3422323d2cd0345499e37ff4cde790bf05513f6b40f5d7de044197980647ef80`

```dockerfile
```

-	Layers:
	-	`sha256:dc27a2565e0de06f88bedc0e8282a81d79116ba6d7c78c2c42e507e23b9042a7`  
		Last Modified: Wed, 13 Aug 2025 00:35:19 GMT  
		Size: 7.4 MB (7415779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af7ac2a06ab32a6110db50194d5b180d35726ac47780ed422c6976fd8c406fb4`  
		Last Modified: Wed, 13 Aug 2025 00:35:20 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.1.1550-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3b55d833556c2987de8eb615fa36f4427f698131a16ec5b8dfcddf76498d3e34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.2 MB (264247169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06b676aa715dc8bb58b8777ed496dffe3c82efebc7027f4a7284b706d62abb56`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7b68ea47bc3cd8615e51fdbe0976cb4999ba56ce8764e755543a4521d69a32f6`  
		Last Modified: Tue, 12 Aug 2025 22:08:57 GMT  
		Size: 52.2 MB (52248409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6978e422a603f55c10edbdbff2aef6a2a5b1bc52fcf21a4f30138d5fd0059bb`  
		Last Modified: Wed, 13 Aug 2025 14:12:27 GMT  
		Size: 142.5 MB (142460557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304162a6513686d78d9053e39228155791b4f0e0804451cb5039e790d488b6f4`  
		Last Modified: Wed, 13 Aug 2025 14:17:25 GMT  
		Size: 69.5 MB (69537561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe0d6f6232b13855591ea3711e3d0e03b2a746f717bdc017bd216b1ebcac0b0`  
		Last Modified: Wed, 13 Aug 2025 14:20:33 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1550-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:66b8190dbadca494447e7fe10fd90ce9c9787e6b156161bd395c1c5d011cc8d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7435866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a434df42db9d1323af72120d6ddcf308c243f5872e6a425c0e966b1f2ccdb56`

```dockerfile
```

-	Layers:
	-	`sha256:e238b081b213b9efb5bb2364bdcba05b24f0ec7c4d08dfa9263301a8925f04c3`  
		Last Modified: Wed, 13 Aug 2025 15:35:20 GMT  
		Size: 7.4 MB (7421496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a93556607d80e6633b82ea9ba00936317defbcd96709f581cf18954fdd7d387`  
		Last Modified: Wed, 13 Aug 2025 15:35:21 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json
