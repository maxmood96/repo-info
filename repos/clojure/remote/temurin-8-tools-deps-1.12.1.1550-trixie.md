## `clojure:temurin-8-tools-deps-1.12.1.1550-trixie`

```console
$ docker pull clojure@sha256:b79d85e9cdf15fa5dad55000cfcf3d4a0d0af94432bfa1353fb083ebfae1794b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.1.1550-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:239ac3b9887a20cd580b75e01061430eab0c477f3bc88e5c0a89022e99258860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 MB (192170723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cbb79dc4a31cc6c4a128dc433bb52d00035e0fb93e0f0e8a425f6f2b6182a70`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1747699200'
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
	-	`sha256:b8364400c35b20e530ea76455b7a73bf615b17d9d6734e0c2539034d9fe0bed1`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 49.2 MB (49246908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ba2954eeb99b2c50175c0d4fa311756584addc8bf70f1b908370b71d22e603`  
		Last Modified: Mon, 09 Jun 2025 17:18:06 GMT  
		Size: 54.7 MB (54716184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06937de4866d4f7ca9e822fdbeb32da09ddf13b926db9c9d65e453cc6ed01e64`  
		Last Modified: Mon, 09 Jun 2025 17:18:11 GMT  
		Size: 88.2 MB (88206986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d9970371c1c0d52021254b99c29245f53d908e4b3f7e46babb0b889d5206495`  
		Last Modified: Mon, 09 Jun 2025 17:17:55 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:582528af19c5c9f51ec6cdc5f7caa8eaf590835495f7186dfd8fe900614bb3bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7594456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2acfdf5074a1d006882fa87e5cfdb3345f4bbdb86b328821d3f80f6876f46b54`

```dockerfile
```

-	Layers:
	-	`sha256:48f6535d4b38a34e70460b11061f02383c0564c9aa8b16074154042c104f6611`  
		Last Modified: Mon, 09 Jun 2025 18:43:41 GMT  
		Size: 7.6 MB (7580245 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e790d8fb8192484992b5909bde3248413265009503349693963066df3d82a21d`  
		Last Modified: Mon, 09 Jun 2025 18:43:42 GMT  
		Size: 14.2 KB (14211 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.1.1550-trixie` - linux; arm64 variant v8

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

### `clojure:temurin-8-tools-deps-1.12.1.1550-trixie` - unknown; unknown

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

### `clojure:temurin-8-tools-deps-1.12.1.1550-trixie` - linux; ppc64le

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

### `clojure:temurin-8-tools-deps-1.12.1.1550-trixie` - unknown; unknown

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
