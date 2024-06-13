## `clojure:temurin-22-tools-deps-1.11.3.1456`

```console
$ docker pull clojure@sha256:6999fad1cfe9041d8cb5d9044cf501ae6ad1afd40097dc83ead727635e1676e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-tools-deps-1.11.3.1456` - linux; amd64

```console
$ docker pull clojure@sha256:09d7384235cd8da2671a1a85d2adf29692dd151053f0380e212f3acceb99d90d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 MB (286587545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f75a4fae10fae10067e4f98ac260a4fbc4fe4631ba6f5453cda166c14e26df8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:b532f8e401e9a1fcc2ea1fc034adf820a5269c6ace45769f60a81fcb673f01b8 in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fea1432adf0957427b45b0ef8e37cbfe045b7cf8c15e3f43e48f2f613e214d16`  
		Last Modified: Thu, 13 Jun 2024 01:25:07 GMT  
		Size: 49.6 MB (49576643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0c9269d331471e8026c4756fe4ac86b5e869a7f1a5b7d7880c41df7fb1aa42`  
		Last Modified: Thu, 13 Jun 2024 18:14:17 GMT  
		Size: 156.7 MB (156715503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0906ea89850a925a62b9c489f409a7404e44bc86afe6b275fa79ce2389db684f`  
		Last Modified: Thu, 13 Jun 2024 18:14:17 GMT  
		Size: 80.3 MB (80294352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a68198b751c496af7e87df6acf9fb44819afba03fc107b90d0425490c0fbd6`  
		Last Modified: Thu, 13 Jun 2024 18:14:15 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8afbdcdcab74f72c18f25eeb817e4f080c190d6d717e6ade84984bfe3422daae`  
		Last Modified: Thu, 13 Jun 2024 18:14:15 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-1.11.3.1456` - unknown; unknown

```console
$ docker pull clojure@sha256:fc90dacade0018c0624e4d45c030136ab8f1e706453d9eb79768925726b8b890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6977467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dc4833ee7fd70a4976ce5104c9501517f50fb26d0d5bce7d8b9c7f2e9da49fd`

```dockerfile
```

-	Layers:
	-	`sha256:0fae510ed071f56cb51003fc6564e4137fc59567d55b41635751d1818d46fa37`  
		Last Modified: Thu, 13 Jun 2024 18:14:15 GMT  
		Size: 7.0 MB (6961344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84c7065ae19bc79ab005a6a267f29acfd8a8a9a1e18c1df11144fe59a6de5fde`  
		Last Modified: Thu, 13 Jun 2024 18:14:15 GMT  
		Size: 16.1 KB (16123 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-tools-deps-1.11.3.1456` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7d09b526f2dad0be20a27aff976816da1c4ba077ca4490f2d31ada3e52161907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.4 MB (284397055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72fdd5bd88f49b42e67a6461e88d565c28ac4a056116826c285276a3691f508e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:cfc8f76c8181d3ae6dda16ae894b184c69dbba114d446426e466126fe0ae62e5 in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1e60a453843e00d6f3d4242dbd696365f0894e3ca2f02f4ce1ab098d7ff7907f`  
		Last Modified: Thu, 13 Jun 2024 00:42:50 GMT  
		Size: 49.6 MB (49613402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a7de9ee68abedc6c5a307899774444d3faa4324c90df9c8bb81d7c84f33414`  
		Last Modified: Thu, 13 Jun 2024 11:59:37 GMT  
		Size: 154.7 MB (154738035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:700d1b3ef1da44e6e96f3ba993d36f968ea1a8ce71de573c05b2b4ba87f4b030`  
		Last Modified: Thu, 13 Jun 2024 12:03:16 GMT  
		Size: 80.0 MB (80044571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f2425113bbd696cb4e059bc20b86840300e4fa5503e4fc2b84e6b75e1734cd`  
		Last Modified: Thu, 13 Jun 2024 12:03:13 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f1e3a0b8f135dca52f9913b27d27f3f813b7e29e421eb606e1ef99cdb8c451`  
		Last Modified: Thu, 13 Jun 2024 12:03:13 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-1.11.3.1456` - unknown; unknown

```console
$ docker pull clojure@sha256:6bbea5642e92098ca260374db7b2529d3f18f093007d3bb65839d9448449cfbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6984437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb57a8a5db454a905eeba35f507abbf68b33d2ee898012aa25327fae98237d9f`

```dockerfile
```

-	Layers:
	-	`sha256:fb2a0720afc0f2141a75d2273474d53178626e2351bb34d1e17a70f06c3bb4e5`  
		Last Modified: Thu, 13 Jun 2024 12:03:14 GMT  
		Size: 7.0 MB (6967755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c836e2dc742b683315db1fc9b5442de6d214487bbfc00c5e4587deebf997400f`  
		Last Modified: Thu, 13 Jun 2024 12:03:13 GMT  
		Size: 16.7 KB (16682 bytes)  
		MIME: application/vnd.in-toto+json
