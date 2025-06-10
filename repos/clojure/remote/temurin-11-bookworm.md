## `clojure:temurin-11-bookworm`

```console
$ docker pull clojure@sha256:01b53bf438615ef3e3d1d50ee15d922ae4f0c81bbe81e59c7ecf4c239ac02ee7
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

### `clojure:temurin-11-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:43b444d106c1d2e3e820d52af094f69dce8628a183c1f21d3a5b0e29a75a3033
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.1 MB (275118309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3ff7e6e16f080a94a31e425cb80e6c2e9dd71ce840b329097de5c5c5c72dabc`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Tue, 03 Jun 2025 13:30:19 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916e1c355185c1fc47b63d945dbf857775811747210510f0c8eacef6a412ffe9`  
		Last Modified: Mon, 09 Jun 2025 19:57:49 GMT  
		Size: 145.6 MB (145635675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbec7399c62fa6d8f1a960dbf8820245df7b37a402239f0bc216dba01ebb2716`  
		Last Modified: Mon, 09 Jun 2025 17:18:33 GMT  
		Size: 81.0 MB (80993744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b32fecdfa9fbcbcf21976a810028d20563a32e6bd439c5f631b07f0374fc73`  
		Last Modified: Mon, 09 Jun 2025 17:18:24 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:6f41544455b93c2ac4f399d00d79a20b72eaa6c64faafd75db2c3c638f1ddd8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7401305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:625533717507db9d494d349e870e8767d1e00f9d66ec1de1779475bed59cbefa`

```dockerfile
```

-	Layers:
	-	`sha256:b06ff8216a59916890ca4c88958054f3e6157e80463840db24aa25157c8a663e`  
		Last Modified: Mon, 09 Jun 2025 18:34:52 GMT  
		Size: 7.4 MB (7387053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec84d9eb936626ddffa05a05b629317c0a40b4bf94dcf9ba056409e6c7aef6d9`  
		Last Modified: Mon, 09 Jun 2025 18:34:53 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:acba0cddbad11d722a6493afa6cbe45c30e3d834d424e7d6076e73c04e852764
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.6 MB (271596763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d6d13c74377d8f4672d4ad5d4cf9fa792e5bb8603f19d24f3175312d0c96a8d`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:1a12b4ea7c0ce04aa0e98be0a8c9942162bac71426f734fe6d3bf988bc9e2627`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07fd337589b0c96f06ac5d8a22e233b7ae5c98928b27c342b7ea0174f5098e96`  
		Last Modified: Fri, 06 Jun 2025 13:20:07 GMT  
		Size: 142.4 MB (142420644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81efd9728c9f144550bb2175a9b45c2759984d22fea4e6b4cef900bd490dd762`  
		Last Modified: Mon, 09 Jun 2025 17:39:20 GMT  
		Size: 80.8 MB (80848293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc555beaa2ac46150a7f4b506cccc39c88aadaf2c31198fa7f9a850a4f5375d`  
		Last Modified: Mon, 09 Jun 2025 17:39:09 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b2a1f2e92277cd6283f46f890aa9f0b955046a84ce7fa221a6f100ba9db2ed6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7407803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae18d357b95c7eda0ba7f0d3197cd10e3c9fad885a238a204fc1cb385dfd6eed`

```dockerfile
```

-	Layers:
	-	`sha256:ed9f831f2d04ed9b10baa849f1109cd78b230aec15ed0b9a218a71c46193d9fe`  
		Last Modified: Mon, 09 Jun 2025 18:34:58 GMT  
		Size: 7.4 MB (7393434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee037db6f82cb95263f87911f2f339c74272b5ac540726ccc3078b63981c66a0`  
		Last Modified: Mon, 09 Jun 2025 18:34:59 GMT  
		Size: 14.4 KB (14369 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:7b858401dfae496e1286ff1fe8f9fb75b2ac7ee83b735f208d637c36eb5686e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.0 MB (271956207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d3fc1343a16b6a2b61ba7de5aba0d761c831c7b9ed37be844ed6933d530d9dc`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
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
	-	`sha256:996840ee350796081b3c80118ca1a58ce8212c6fdf88c454706a16457903a0c9`  
		Last Modified: Tue, 03 Jun 2025 13:33:40 GMT  
		Size: 52.3 MB (52331619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc84d937b9f9c6a8fdf10268fbf36f3f3530d2d16cd85cb8e98d71c60b41b51`  
		Last Modified: Mon, 09 Jun 2025 19:58:38 GMT  
		Size: 132.8 MB (132810522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d57bfb8583c54fbe202b8e8bcc6d0883ed7347ee0174001d0f9a49a6cfd0332`  
		Last Modified: Mon, 09 Jun 2025 17:50:50 GMT  
		Size: 86.8 MB (86813421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04478a98487575969670fd77f5dc87072e2be9049d6aaeebaef0ea6c329596f2`  
		Last Modified: Mon, 09 Jun 2025 17:50:40 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:bd28909e6f8cde1f1c62229a2fa019380448ce7c110e02059be9098bfb39775a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7405942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0007fd90ed581709933bf068b8527c26df5cfe29be1ab470eddc82bfb8ce679a`

```dockerfile
```

-	Layers:
	-	`sha256:5563475d5ba9f434e3c3d653461ec3d4f42efd77bdb5d0c3722484737ce336a6`  
		Last Modified: Mon, 09 Jun 2025 18:35:06 GMT  
		Size: 7.4 MB (7391642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffc3b5b1c2873053f8693210a9af87331ddde0cdf7a0179087db4be39714a6c6`  
		Last Modified: Mon, 09 Jun 2025 18:35:07 GMT  
		Size: 14.3 KB (14300 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:6850435dbec5a91c498b1fbaccbdc03f84d7f85acb168209ee9f328468e16a52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.5 MB (252532409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4426b2ee092f3961fdc1929c85910a574db3f2ec894c74b836f83fd3ff2fd1db`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
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
	-	`sha256:47f9a2c2279c9df9e222a4c8af501e43b0b5e2552eda9597a97162080b8f106b`  
		Last Modified: Tue, 03 Jun 2025 13:33:39 GMT  
		Size: 47.1 MB (47143842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86c88c5d926257cdcfb8a6708039fa40a0a893499f3bc0262b7011bfd58b087`  
		Last Modified: Tue, 10 Jun 2025 11:56:20 GMT  
		Size: 125.6 MB (125585354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f3c3754859ecc7afec3128793903e930d5b07abc17ceb4f59639e9cd0bca3c`  
		Last Modified: Mon, 09 Jun 2025 18:41:10 GMT  
		Size: 79.8 MB (79802570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88764e6b8c3655181d95d9ac211a03100d7bea7c862a6cc32c5e434b30436e6c`  
		Last Modified: Mon, 09 Jun 2025 18:41:04 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:a01b16bbaa9c1b9d53302d348d1f79d81ab4e429268606aaab836595b23675ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7392628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:912c3fc83d440ce834622ad2be3523b71f8102d99430115bf585a6ebeba273da`

```dockerfile
```

-	Layers:
	-	`sha256:32fd20b6c54a71d13b658c54a004e60ad14ed725e62150648876819dbb61bcee`  
		Last Modified: Mon, 09 Jun 2025 21:34:48 GMT  
		Size: 7.4 MB (7378376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d255ae28e0754bbec91dcc20fe4fbf25d828ed410df49465a4262269406d26f`  
		Last Modified: Mon, 09 Jun 2025 21:34:48 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json
