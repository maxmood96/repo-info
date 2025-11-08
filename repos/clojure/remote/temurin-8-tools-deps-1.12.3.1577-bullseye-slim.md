## `clojure:temurin-8-tools-deps-1.12.3.1577-bullseye-slim`

```console
$ docker pull clojure@sha256:5918e47286c22a5eee1499e0c285e379a419ce2b7abf6523da7f51e18abf8240
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.3.1577-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c9e08194e182e91b3dec2b9448903a4ed1bda3335bb4bed4882ce4c7f5971d3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144144818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29864b332a53453a19fc6469fd73fbf437a4978c5ad48876a04b7f4213fb7a27`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Sat, 08 Nov 2025 18:04:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:04:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:04:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:04:18 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:04:18 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:04:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:04:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:04:32 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:cf5f39ef3fca9730ed04aee5f10040ea152a9793dec0d626f4205eeac5ec3fc0`  
		Last Modified: Tue, 04 Nov 2025 00:13:10 GMT  
		Size: 30.3 MB (30258596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e30d2a31cf22e696a6f77979b5fa70ed79d3f7a1873c975da535f89c95824b59`  
		Last Modified: Sat, 08 Nov 2025 18:05:20 GMT  
		Size: 54.7 MB (54733369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77ea038c5312878a080ec3c443f243f12a73f5a357bc216e3728b4035678458`  
		Last Modified: Sat, 08 Nov 2025 18:05:21 GMT  
		Size: 59.2 MB (59152209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e02e5b4a6ddd5215560d73ed8faeb519554f0faf695e96c1188e5a368e9a6367`  
		Last Modified: Sat, 08 Nov 2025 18:04:58 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.3.1577-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dcad16c17a5b53fe2a32a2b99e9255d4d3ed059253d50f661691e66fc7430a7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5443925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e77209e50b1c54d843b4be9d4eabdd47268bbbf588b957993d5278796ac1930`

```dockerfile
```

-	Layers:
	-	`sha256:2ee157b61ab0afdc1c68b7b9b1aea2d85e7aece829eea186984074776667f065`  
		Last Modified: Sat, 08 Nov 2025 19:37:59 GMT  
		Size: 5.4 MB (5429677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6a9cfa810c391454d99313dfcec814384bbc08f7fa6edcbfcf1f652b92cba44`  
		Last Modified: Sat, 08 Nov 2025 19:38:00 GMT  
		Size: 14.2 KB (14248 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.3.1577-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:87f650d403193f045425bfa001e13ab5496cf7a239c1ac9f85298e56b6421a7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141851870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:784e02ae91e290a0a5120b19ee224538ae0877e27994159f68d0afc9fd7e0073`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Sat, 08 Nov 2025 18:02:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:02:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:02:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:02:46 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:02:46 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:03:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:03:37 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:03:37 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:241077dc995c26590e89ca59e622bf97509f2613a9e84e3e745225e4259eb511`  
		Last Modified: Tue, 04 Nov 2025 00:13:03 GMT  
		Size: 28.7 MB (28748552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c06e7520dc506293fcc0035fa134fd0b5b845c8c02cf920987a2ae809c64239`  
		Last Modified: Sat, 08 Nov 2025 18:03:30 GMT  
		Size: 53.8 MB (53815012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a843128c4604356836e66293086aa41ae2f16b43ff4596fcebe6685572e53f9`  
		Last Modified: Sat, 08 Nov 2025 18:04:06 GMT  
		Size: 59.3 MB (59287662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767bffe656fb691db81c95bea782a44434f96eee606372d5fe38322925101bd8`  
		Last Modified: Sat, 08 Nov 2025 18:03:57 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.3.1577-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:99afe4985840914cc30c7890e4d56d7d18cd0e25f5b42737d237e4cb08deb183
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5450473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81e08d82668adcfccb394361446b7290abfa55c591646f820c24272580df49fa`

```dockerfile
```

-	Layers:
	-	`sha256:53c028bac812371460b9b78b7769c7de61a0e729d085c65eecb5b506d9f7e38f`  
		Last Modified: Sat, 08 Nov 2025 19:38:05 GMT  
		Size: 5.4 MB (5436107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:300ec9455316f485260369ba5721288f94c37aa488728eb6467aae70866d736f`  
		Last Modified: Sat, 08 Nov 2025 19:38:06 GMT  
		Size: 14.4 KB (14366 bytes)  
		MIME: application/vnd.in-toto+json
