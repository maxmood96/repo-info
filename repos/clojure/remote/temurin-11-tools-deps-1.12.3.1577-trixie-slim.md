## `clojure:temurin-11-tools-deps-1.12.3.1577-trixie-slim`

```console
$ docker pull clojure@sha256:31d86f099c6ad4ed4fbc5749b6bdb972702bccd0b97884c0fea9f1d0d3f8fc20
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

### `clojure:temurin-11-tools-deps-1.12.3.1577-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2f94a11f251c7d7031fae90dcbb033edb85ea131bde5fb1edd6615ab63be4efa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.4 MB (250375170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcc166f6071ed6bdfecdcb2bccb3a4f85c214898afdd22d1c500298639cb99e4`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d1d8ace96aad2c38ae1b6bc9571a6a4e4d7f3867f4a1d781e4ddc2358a32fbd`  
		Last Modified: Sat, 11 Oct 2025 04:21:58 GMT  
		Size: 145.7 MB (145658312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81949d27516b4003afb770367c5799e3ba9e012a16b445648d788f1d526fb94`  
		Last Modified: Thu, 09 Oct 2025 22:28:12 GMT  
		Size: 74.9 MB (74938446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45182f4fb74d82dc9a04bc8601ef0f49ea12bc431763f6d9d9b216811aed7e31`  
		Last Modified: Thu, 09 Oct 2025 22:28:03 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9ae80ac0c683399b05b0c3ae946bdf4954fe2113de133f5ca46b2d87f602e89d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5290594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05722fc032e8457f65d2f775f29ecf729703e37eb0bc173087784a51bb1f71f2`

```dockerfile
```

-	Layers:
	-	`sha256:3545555c1d667ea87dd85194fb13c1e661e29715c7e54231a1f054880b81ba7b`  
		Last Modified: Fri, 10 Oct 2025 06:39:01 GMT  
		Size: 5.3 MB (5276308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:094ed35cd24845d2854e727d614002ddf846e0bfe0a82f209ef066c307687b21`  
		Last Modified: Fri, 10 Oct 2025 06:39:02 GMT  
		Size: 14.3 KB (14286 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.3.1577-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9582153fa792f1a98e0cea75d58975c8fd5d8038968d08a6d14ac573bf4ec1b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.7 MB (247726706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:709f4c73a2911eef824830910845a80ae7b58c5ae39754522823b990ae74102c`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:618d75423bce1f565f31b6086da2409fed7b62cc1272cc1c7ca82825345236df`  
		Last Modified: Sat, 11 Oct 2025 04:22:55 GMT  
		Size: 142.5 MB (142460559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7db1bcff211b4716c1b731b1c304c846d70e49aa945c7c49067f4c6147b3e0`  
		Last Modified: Thu, 09 Oct 2025 22:28:13 GMT  
		Size: 75.1 MB (75124659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee4136eea81a71f3e2625c7f55ae63608419035d699b1ecf54b2fb0c1f40da8`  
		Last Modified: Thu, 09 Oct 2025 22:28:04 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a11dff6b154040e7e18f57c2bbf5561f0127fcfdf28b422b1656b6c8fc6c37f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5297099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8b6bebcf3c6b4ef4c8da7b00c0e51b46b4c9ba2a4dafc73cc25a7b138b78243`

```dockerfile
```

-	Layers:
	-	`sha256:b2d1d340b818b3b7a22b4d6d8728bf219d29f4683b6ac12f621ab37f3b8fe3a2`  
		Last Modified: Fri, 10 Oct 2025 03:35:08 GMT  
		Size: 5.3 MB (5282695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5275abda392de28baa84e0bce02aaf7abc7e46599c6825e988cb570330635ea2`  
		Last Modified: Fri, 10 Oct 2025 03:35:09 GMT  
		Size: 14.4 KB (14404 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.3.1577-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:479b685c77b99b26d71507af2e3380663ac04fd7ce494cbc08677f65f24e6f0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.0 MB (247040498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c46fdff075ec3546fd52df214c50e75522fde792f8a480e4342e2482a66959a`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8bcecd3ced4047f6a4d35464fc2ee9b45e7fcc10b49690427794f4421b0552ab`  
		Last Modified: Mon, 29 Sep 2025 23:41:19 GMT  
		Size: 33.6 MB (33598454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88380a6dc89f1e9cf766d25537e1a885541867d4cddeb508771783051000e69`  
		Last Modified: Fri, 10 Oct 2025 05:04:34 GMT  
		Size: 132.9 MB (132853211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e930004931e5d784f1ebfb65004f8d78c4aa63523d5593c2121049760de60195`  
		Last Modified: Fri, 10 Oct 2025 05:14:11 GMT  
		Size: 80.6 MB (80588189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d584c29381dc1d0058c44ba0b758c8ab9354ebabfb4a901e1de1f37dbfbd00`  
		Last Modified: Fri, 10 Oct 2025 05:14:08 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bb34c9095ac0ff0c3bb3427f54eaa43b1ea26eed009f064c35bf295f3a2e3883
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5294398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:620f5cbe5380fa8ee921a17459cd5b96289182b78a433202f83b8d8c22053eae`

```dockerfile
```

-	Layers:
	-	`sha256:988cd5165c1dc2efa41d3c6f8b8dedc8c4dcd3a53eab919a76732c1f37de5b77`  
		Last Modified: Fri, 10 Oct 2025 06:39:10 GMT  
		Size: 5.3 MB (5280064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cd0e94f8c3dad362a12401f359d2e25a33672cefc22a35b93eca3a34efd749b`  
		Last Modified: Fri, 10 Oct 2025 06:39:11 GMT  
		Size: 14.3 KB (14334 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.3.1577-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:4dcce88ed2952a5c50f91b0ff0d4e2897d27f6a44114a48df17da82da9ce1cd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (231022562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:388886c630afb8aca49ce0c1059f4a6cc9b7041696191c42b1f55af8b24baecb`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:924b0740f35a15fc20142be5c392f6b033c8051daecf16d2db38c22d6d73eb53`  
		Last Modified: Mon, 29 Sep 2025 23:41:29 GMT  
		Size: 29.8 MB (29837230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e79b5900b5effeda4776d69d4a251c63021d33a0ee35fa09174f72fb2c2348d`  
		Last Modified: Thu, 09 Oct 2025 23:01:47 GMT  
		Size: 125.6 MB (125622160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e28ad475e5850d31559ad5a4a4fd8a122056358bbbcbb146901f63fc424b46`  
		Last Modified: Thu, 09 Oct 2025 23:07:31 GMT  
		Size: 75.6 MB (75562527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341fb9185caaf29f861e138acceb05af227fe4253b0af3fa7442eb60493a3132`  
		Last Modified: Thu, 09 Oct 2025 23:07:19 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ec7c30648c2b7946cfbdd52b9fabd7f67f873da8995c3d970b7daf693b5a2454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5286521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad25d428ba507bacee76b7cbef4221054c7f2eb97a3fec9a7f712eaa7a7d8ec4`

```dockerfile
```

-	Layers:
	-	`sha256:42e553ca624159931c3989469da2f188896ec5318d323b25eb4b32ea28f7fd8b`  
		Last Modified: Fri, 10 Oct 2025 00:36:45 GMT  
		Size: 5.3 MB (5272236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b500d9ed0593c91fdc203b5ab1f6e68d564230fde0674c83800ee3c73814cf9`  
		Last Modified: Fri, 10 Oct 2025 00:36:46 GMT  
		Size: 14.3 KB (14285 bytes)  
		MIME: application/vnd.in-toto+json
