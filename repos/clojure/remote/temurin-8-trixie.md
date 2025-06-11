## `clojure:temurin-8-trixie`

```console
$ docker pull clojure@sha256:d7af73232966bd0360d1a045cf37a356849d1353b724ff2007e37d9fd77659fc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:6e6cfd9e08266160ab8759c3601bd789fd9b1dfd0545aab71cebb781f6b6762f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.2 MB (189235993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55a3425b97be942dada080eddbf230fe9cb3d453a7cecb07f4593ae9d77c2532`
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
	-	`sha256:d8e51f6b7dcdaee60f07f9a13a971abe1be9dc977d52d0849087118f80a1c7d6`  
		Last Modified: Tue, 10 Jun 2025 23:25:45 GMT  
		Size: 49.3 MB (49253859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ded4952a75061e537ce5b6b0df59cdb642c50812c190ce00881d9e8b3cc371`  
		Last Modified: Tue, 10 Jun 2025 23:50:27 GMT  
		Size: 54.7 MB (54716149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c4e2b2d3ed457e9f86347ea4d14be6e4071515aa40eb84a99c492ae182c807`  
		Last Modified: Tue, 10 Jun 2025 23:50:28 GMT  
		Size: 85.3 MB (85265343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a94dc2eb92701500e31f31cd160697a10b09cc26a2345dab1867ac61d5ad240`  
		Last Modified: Wed, 11 Jun 2025 01:30:36 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8a01459198f74e68c96ebd4665ca83e5c389b2d2c527526e22f2e42dc232b48c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7594972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b4bb74e9dc4387373ae9607c47ee464a79e9c193a6454165ec8ec3da1a779b`

```dockerfile
```

-	Layers:
	-	`sha256:5c4dec3f97ec2c7e93a8739e97390d5930f429dd3a5eacac8c2be49a483caefd`  
		Last Modified: Wed, 11 Jun 2025 03:42:29 GMT  
		Size: 7.6 MB (7580759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b823c0147583c806c2da104f742051aea65604e403db6bd2a9211223a289fef`  
		Last Modified: Wed, 11 Jun 2025 03:42:30 GMT  
		Size: 14.2 KB (14213 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:08db0ade878194c27f7b2f93aee6864d2593c3b9e8b145c028378af3c1d075b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (191960238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5230b2edf5d26d2dc10bb6c3a74e513addff2668ba72295f735380536cec307`
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
	-	`sha256:397826b9fe635f12caff1a603eb12c37426a5b3dc563e0adff2debff0c68a6b0`  
		Last Modified: Tue, 03 Jun 2025 13:47:15 GMT  
		Size: 49.6 MB (49618294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62b438f9c0792eeeaa8637b24f8c401b4a12e19eef04c099112c78a727c9bf9`  
		Last Modified: Tue, 03 Jun 2025 19:21:35 GMT  
		Size: 53.8 MB (53830517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b38f6ca23a243df486a72221462a363b7ba8a913339566c7345560a04fc4a00`  
		Last Modified: Mon, 09 Jun 2025 17:38:06 GMT  
		Size: 88.5 MB (88510780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b002f82b2c13f529db4b4d9b2a2fba51d39c018e2323e414f632454c7669a97`  
		Last Modified: Mon, 09 Jun 2025 17:37:43 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:527d3032822e119cd17b905d14503b7004b22fc4b923a389e0d04a3a29390d0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7602304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f076405117889631470be94da357aa6c9d4ff9c80c22a4d35d4c34eef949b257`

```dockerfile
```

-	Layers:
	-	`sha256:2b30c2be2d7253a0457e024d406f4947ae7b3c1c031515213e4482bf26b1c1e0`  
		Last Modified: Mon, 09 Jun 2025 18:43:49 GMT  
		Size: 7.6 MB (7587973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a071a798a4ce726e08bab6982578cf4f52e23a37c30df3f3c25a8039108cde0b`  
		Last Modified: Mon, 09 Jun 2025 18:43:50 GMT  
		Size: 14.3 KB (14331 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:c2f19984590ffc860b260ee151f7d1018572dfcdd3ec5d51ee971e3864c11aca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.2 MB (199200006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcc513a5f2744d03db657429c6ba9bc23318814a640d597a0ffbbbe547343328`
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
	-	`sha256:25dfffa4126a91eb76c700c90bfdc9a9e15f34c7438a81f16c8a6999bbde6e45`  
		Last Modified: Tue, 03 Jun 2025 15:03:14 GMT  
		Size: 53.1 MB (53080544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f975f5c873cd794ffce77448d785fd1ca79428164a5e8dde7131d18ee75ac676`  
		Last Modified: Mon, 09 Jun 2025 19:06:31 GMT  
		Size: 52.2 MB (52167951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004faf52cc88e9d34177ab8476e4fd8ddb28728b5e7ef76cb272573aa69af857`  
		Last Modified: Mon, 09 Jun 2025 17:48:00 GMT  
		Size: 94.0 MB (93950865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3421c2cbee89c410f6c33420c22e73a24ae2966601f44566fbf9041dc7d48afc`  
		Last Modified: Mon, 09 Jun 2025 17:47:39 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:cc9602d1505878636f7b83bc6a828abc494e823a238ed1fec19a2c6e348f1ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7599515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6856cd5fc2d994c2dad29c880b8dd2028520f63207d0d92a6e8415046b14b04`

```dockerfile
```

-	Layers:
	-	`sha256:2745fe2c3ee7c6377e62c6cb3623fef8072f689226472e33c5215f598697d379`  
		Last Modified: Mon, 09 Jun 2025 18:43:56 GMT  
		Size: 7.6 MB (7585255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95ca9b3d2a439b2a7699d0193512b37dcc284ad10f121b54d64ebfda75e1f0c2`  
		Last Modified: Mon, 09 Jun 2025 18:43:57 GMT  
		Size: 14.3 KB (14260 bytes)  
		MIME: application/vnd.in-toto+json
