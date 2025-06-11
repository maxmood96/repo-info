## `clojure:temurin-8-trixie-slim`

```console
$ docker pull clojure@sha256:11234e838b648677f5f566724d1c06d0edd2edbebfab5b4114a4466cb82a667e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b9687b95f2e98cb223fdf0d6e50ccffc37532c6c417f06553963d3964859623a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156195148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ef690d6f5ca8293bd4afda1feb0ba2b6faf2b6b31e38b46f37953e8ff9bebb`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1749513600'
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
	-	`sha256:6f052c0ff895d860a8f6983dcf5207c5e8ff5949529101bf68c1e92e9c8baf36`  
		Last Modified: Tue, 10 Jun 2025 22:47:31 GMT  
		Size: 29.8 MB (29756816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d38d76df7740839a0e23aae7309741f336f78faf1d8b3a527ec12bfe645f4d9`  
		Last Modified: Tue, 10 Jun 2025 23:50:35 GMT  
		Size: 54.7 MB (54716149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3388db0dd84792400f70445061a99b9ae2ee88f8cd733a5b704f6abff3fc51ce`  
		Last Modified: Tue, 10 Jun 2025 23:50:35 GMT  
		Size: 71.7 MB (71721542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:947549eaba1fd66e170ef48bca196f178ca4cc31b218967d30001a4d067b91f6`  
		Last Modified: Tue, 10 Jun 2025 23:50:30 GMT  
		Size: 609.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:18599d4a2905b6890442de339c9313b717c3ae3da0391d347e456bdc1fc2e837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5388679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f2e93b8212ec73b9a6145f46d64ec4c3f3310dcfbd5961293b0c5399656fe0e`

```dockerfile
```

-	Layers:
	-	`sha256:b6dcb288492aaa478356d66b0deab33cc3941e5c818e070e213ce8a2f2a5ef09`  
		Last Modified: Wed, 11 Jun 2025 03:42:32 GMT  
		Size: 5.4 MB (5374408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:155d4dc14b706374155d9219c268332a826b50b5437a4a749c4e2eff4b71c35a`  
		Last Modified: Wed, 11 Jun 2025 03:42:33 GMT  
		Size: 14.3 KB (14271 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:84b573cad05a7330fe695dc7ae7a697ecc8132351a2f4116e7ba77ec12e0d05b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.9 MB (158918158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9be7143c6fe1838c66ef723dc01b9795f55b4f9b86590fcf96aacceb2ea6ad7c`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1747699200'
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
	-	`sha256:6098c2c9fa277c00ab580ce12bf64a9e1edf9e9139ba18ad85f3cc3063834aa6`  
		Last Modified: Tue, 03 Jun 2025 13:33:56 GMT  
		Size: 30.1 MB (30119455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3027bac347196f3028d06f80221ee420e9ad855e5c00339bbfa0557a9ae2305a`  
		Last Modified: Tue, 03 Jun 2025 19:21:10 GMT  
		Size: 53.8 MB (53830502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ba6fbac49977f91971d6fbae927e16d3df1ec2ede5e6bc2203875177eb11f0`  
		Last Modified: Mon, 09 Jun 2025 17:38:34 GMT  
		Size: 75.0 MB (74967555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d4338b7048c25de8778024102c1916e7f0871143f4e03c88b035d3f6cf7c78`  
		Last Modified: Mon, 09 Jun 2025 17:38:22 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2630d2df065b6e936e806d132558518e203b3ecaa21afa137516604f9992dd23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5394750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:993712cd678d0aa08850facfc9290038abdf208bc12bb4b7fbb0b93866bf0187`

```dockerfile
```

-	Layers:
	-	`sha256:9bd831e577f76e6ce817e24407f08fea84e37460b3e8d70e4a991d95a6dff0bf`  
		Last Modified: Mon, 09 Jun 2025 18:43:56 GMT  
		Size: 5.4 MB (5380361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:615573a0aa51a6aaf0418fbfcd6d21e3865314cca9c265720d2d7406cb1eb624`  
		Last Modified: Mon, 09 Jun 2025 18:43:57 GMT  
		Size: 14.4 KB (14389 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:ec89c320f419481b3d3bb9bd896b9a55db54839c859bb0133eb36b3620040051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.2 MB (166151203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdf2465e1c9cb642038b763bfec9cb89adf08d4445c1b668bb906c4d2f9f72a3`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1747699200'
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
	-	`sha256:62eecea9deba6eaccef3e829ddec51f2c540dbbb668a68816c8ce3c4b8023d93`  
		Last Modified: Tue, 03 Jun 2025 14:07:09 GMT  
		Size: 33.6 MB (33580565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed347681401881a3761af3b137e387f41b112bad5ebb9315d39c8eed38c8394`  
		Last Modified: Wed, 04 Jun 2025 11:31:14 GMT  
		Size: 52.2 MB (52167965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:740188ead1a3f5733911c605663f6a78a23d22e8ccf8e9a391400738fdaf7e01`  
		Last Modified: Mon, 09 Jun 2025 17:49:35 GMT  
		Size: 80.4 MB (80402030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fbce661df18a144e467ca575c5b0b0e87708b10f3dbaac3aebf7578b8fd8ab5`  
		Last Modified: Mon, 09 Jun 2025 17:49:23 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b6597c33d802f04c4feb15b773a718bb73533ff098f15603137adabae64b6168
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5393177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c66f3736fb7a5bbe792870ed3b328c5e570e5760241a8bf26a909351178a882f`

```dockerfile
```

-	Layers:
	-	`sha256:8147958767cad187514bceaa9962b56e9cf988faa4e28ba818cea3d01464935e`  
		Last Modified: Mon, 09 Jun 2025 18:44:02 GMT  
		Size: 5.4 MB (5378858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c0f66f504a1daf2ed501d428397830fd30b1a985084f10bdb0d12ea92d81ef3`  
		Last Modified: Mon, 09 Jun 2025 18:44:04 GMT  
		Size: 14.3 KB (14319 bytes)  
		MIME: application/vnd.in-toto+json
