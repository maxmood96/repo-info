## `clojure:temurin-11-tools-deps-1.12.1.1561-bookworm`

```console
$ docker pull clojure@sha256:ef355f92cf9aeae7306a674370ec6ce612a1a09b1e480f2eb0a5aa6127a87383
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.1.1561-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:08dd8d3c9316c7ad1dfb76191f50851f7b747c989a539bc63df8134a1f81283a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.2 MB (275195761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e05b51d47e2feb1b0ce6c97b9b91838a1a42eb75a388b20663758984ca134704`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f014853ae2033c0e173500a9c5027c3ecffe2ffacbd09b789ac2f2dc63ddaa63`  
		Last Modified: Tue, 12 Aug 2025 20:44:32 GMT  
		Size: 48.5 MB (48494511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d954a7092c7fe4173bec7beb95fddc73b4dd135a4eeb862851df4b2a26fb8b3`  
		Last Modified: Mon, 18 Aug 2025 16:52:23 GMT  
		Size: 145.7 MB (145658205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68eba7c641003d549067e28909093c24561f6a22f07286ab2c38616821e3259`  
		Last Modified: Mon, 18 Aug 2025 16:53:10 GMT  
		Size: 81.0 MB (81042400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dce571d6ef42513527409b85f4e9fdcb1b4fa7ac93f8dc2e08c372e589106ae`  
		Last Modified: Mon, 18 Aug 2025 16:52:56 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1561-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c8cdad848a3718650a75b1cc67f75dba0af3b3768a39db329e568ee0f65ebf39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7402690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79fa4f8ad2560b1cd4f1d1d3afbb4805f58e8d343f7c1705b83b98e746a8d80d`

```dockerfile
```

-	Layers:
	-	`sha256:f79027eb07427d6b4a716ad3e6204fc79f1f47cd984bb544dafc4170434a7c69`  
		Last Modified: Mon, 18 Aug 2025 18:34:57 GMT  
		Size: 7.4 MB (7388438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d5d6d9d78ac85d1d8832db14b72a1fe673f6f7acd6d062c7cd0fa10c3d4a5a6`  
		Last Modified: Mon, 18 Aug 2025 18:34:58 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.1.1561-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b86c846e613c5332be28c2f4cad7434322e868057a533ff77f3d80bb4ef685ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.7 MB (271717289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1d1dd35e066cccfd330826d33feea7711819e69c7b025c652d1fd67f1a4aa5d`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:35f134665ae4469a16b5b7b841e9efe6b186960e0533131b3603e4816aabeb3a`  
		Last Modified: Tue, 12 Aug 2025 22:08:09 GMT  
		Size: 48.3 MB (48342450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e17e393506147fbd7055e29d89728a0fc86ede72088d0c45d92332a69b6e1676`  
		Last Modified: Mon, 18 Aug 2025 16:59:28 GMT  
		Size: 142.5 MB (142460572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0fc9d97567ff17767e414dcac934f947994ba7fadbe1826d1453257f7c6fe96`  
		Last Modified: Mon, 18 Aug 2025 17:00:03 GMT  
		Size: 80.9 MB (80913621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d998cdad38477e6aa662248f50bc2547503852f00b89e3704ceb45381f039a`  
		Last Modified: Mon, 18 Aug 2025 16:59:37 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1561-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d2501ae91548efe9b6b16bed342fb2633d5663003be9d9f9018f750d6c392368
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7409189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071b75a32e9c2d4030fc9f440df3ef1808e21437d451a91e403456daa971b134`

```dockerfile
```

-	Layers:
	-	`sha256:f76a1dfd3b0d36a8dee3f20999a69576a16bad88bb1c069319ef39432562e712`  
		Last Modified: Mon, 18 Aug 2025 18:35:05 GMT  
		Size: 7.4 MB (7394819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eece6d898112884f64c6dd5f0eee46c8fcd74d1e9d099c9416561bda9695a8f9`  
		Last Modified: Mon, 18 Aug 2025 18:35:06 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.1.1561-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:faa629028d07eb37aba5a03806aedea1262e3a7fed6f1d3ee125888bfd4f9dfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.1 MB (272061171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19da990b44353891317f062346b66a0bb6e700848494ca112a84a53c55bf3bb7`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:33bc01697f2fcceb00fe53fe1bf433b48dc127c82c1555f61eeddeda9d72ff40`  
		Last Modified: Tue, 12 Aug 2025 23:05:53 GMT  
		Size: 52.3 MB (52338077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0cbc261facd2ea551ba4f1d307ad561b88de934025d4d92da0a46a7a5d5385`  
		Last Modified: Mon, 18 Aug 2025 17:07:21 GMT  
		Size: 132.9 MB (132853318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2a56ebcfe98a124d7159f906fd66599864574c6aa4d7171e9e1b88a0e6c88c`  
		Last Modified: Mon, 18 Aug 2025 17:08:08 GMT  
		Size: 86.9 MB (86869129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673ead3776c5c339ed01aa39278f49943e26bd89108b1976caa78257e0d7881d`  
		Last Modified: Mon, 18 Aug 2025 17:07:58 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1561-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f862ba843825769fc06b82c38fe98ae481e040f46d87b75b7585983c02e29bc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7407327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:357816f1364d9a9d1fa6fa74bfe57f9794cef07177c4c404f98574d244851c1a`

```dockerfile
```

-	Layers:
	-	`sha256:70ef207d15feabf1a7a2efeb6ac1335010be47cc99b6b51f1808e5705e7bb56e`  
		Last Modified: Mon, 18 Aug 2025 18:35:13 GMT  
		Size: 7.4 MB (7393027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3fa08c6c5c8cc86136fa855b524e9a7c2bd16605d6bd7c05b7d3977785a3c46`  
		Last Modified: Mon, 18 Aug 2025 18:35:14 GMT  
		Size: 14.3 KB (14300 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.1.1561-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:1d7758affd3c7c06cc8ee9cf4e24538981b548d596d75fabb4dff26d16d5c179
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.6 MB (252622441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adbe80a28cd8138cb304f1a98c194d76e46cf6504db19764ea8c34f2484c1443`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:635b31fd21bf059b6af0abf57b343066d0218ebb3e0b679927cc1752427a72da`  
		Last Modified: Tue, 12 Aug 2025 20:53:37 GMT  
		Size: 47.1 MB (47149866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7efb0bde79f746db6b5bf0ea02c772ab6b0f4c21efe10e39411b960291cabf`  
		Last Modified: Mon, 18 Aug 2025 17:03:28 GMT  
		Size: 125.6 MB (125622103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a92afbaa5450bf6135769d77cded2e05ba155c917efbb105cfb4933e1991c2`  
		Last Modified: Mon, 18 Aug 2025 17:03:26 GMT  
		Size: 79.8 MB (79849827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8177e139880df2696f259e514753c2371a1e8bd74670585e69eb308680fd68a`  
		Last Modified: Mon, 18 Aug 2025 17:03:08 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1561-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:873c4b8dafbf427a991344d6a63a4a20a7e8638b7186b43d6da4989573140fc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7394013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23490bb644b70f041b373e8d771d7ee614be57e73d43f80ad2ef77014e273811`

```dockerfile
```

-	Layers:
	-	`sha256:dc47103e2b0371a38113b2fb601baff0bf3a2ca64d3cc2d51138e7c91f6fb765`  
		Last Modified: Mon, 18 Aug 2025 18:35:22 GMT  
		Size: 7.4 MB (7379761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:583e79cb6dbbf2185207251dbdfa4a83e7e32daa7ec9273923f321c856e87801`  
		Last Modified: Mon, 18 Aug 2025 18:35:23 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json
