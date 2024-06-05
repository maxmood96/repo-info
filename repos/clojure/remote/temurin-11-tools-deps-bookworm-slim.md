## `clojure:temurin-11-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:d28ff0437cc0776763cf720bf013b5f22378367b6e6925ceef184f251310fa3f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b0ec3041ec2b533fe26d8801b6e96fd822308f57c070a611863e705b32f6f631
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.5 MB (243524793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e001232498fa814087fa81af7b1f08437fa467cecd2c7caae336c773e2c70d8b`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173559f4941d0f6fd9dad904f826952192d6d4459cfee940b5cd84cc874c8df9`  
		Last Modified: Wed, 05 Jun 2024 06:10:18 GMT  
		Size: 145.5 MB (145505194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a88b4981143314111492cabe5ed8f4f5244fa6fee5dfc6ff68838ba36e2201`  
		Last Modified: Wed, 05 Jun 2024 06:10:18 GMT  
		Size: 68.9 MB (68868540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e81540a573c92ee758fdc55b69927e509ac5b146979a23a9885ccabc21581b3`  
		Last Modified: Wed, 05 Jun 2024 06:10:17 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:35c5bbd832b83f9deb041d2648cf8f5363494d05c65456d618e6014fd4094709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4718826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edbc2eeeeabbbe6f5f8ef4246ef03c9183fa9f1b66a829d7376d87b0819ab29b`

```dockerfile
```

-	Layers:
	-	`sha256:343b4604871618d5bc3edfcd1e515168dd82b9286725ae404ba8cf1bfdf1f35a`  
		Last Modified: Wed, 05 Jun 2024 06:10:17 GMT  
		Size: 4.7 MB (4704938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd48f0c5237cd8a6957624c66c2493fbdce752e7e0aba1e88cd2e13da70bdb03`  
		Last Modified: Wed, 05 Jun 2024 06:10:17 GMT  
		Size: 13.9 KB (13888 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dbe4125e2fb8b211e2585e782a39642bf4c8c22ff38fde8616cbb286123f59dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.1 MB (240104864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee9a77a681616033d0c621ebded7d60e5f9c42b970e5ec2fdde545a7d44befa9`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 14 May 2024 00:39:40 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 14 May 2024 00:39:41 GMT
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c790609acff3d7b5f1767ea22e881912e9160eae8fcf8d0acb5a85070b695ad`  
		Last Modified: Wed, 05 Jun 2024 13:53:59 GMT  
		Size: 142.3 MB (142304052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f223fe68953ed68aa0a20eb1e0c6e9f405b6515b3b7bd432693da06f5e56ecc5`  
		Last Modified: Wed, 05 Jun 2024 13:58:46 GMT  
		Size: 68.6 MB (68620659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e697ac14207b98deb0c9e5ed423dae46324311417859003d4c403fae7f86796`  
		Last Modified: Wed, 05 Jun 2024 13:58:43 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4e047f838636807dba099676dd2308ad9333d374fa1497d994e4075f86018ef9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4725751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a47fb57e20ac49b958a4c5884d08aad1f2e81a3758d693709e2cbc5d324bef`

```dockerfile
```

-	Layers:
	-	`sha256:26ea4dfde3f02a4e15745a301271501034529cde50f5d5e8b7f3c99514d10b05`  
		Last Modified: Wed, 05 Jun 2024 13:58:44 GMT  
		Size: 4.7 MB (4711323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e275358f6317c7b5b41ee5631766b28b93b2f179ef3e70e2c8ec49f434682bb4`  
		Last Modified: Wed, 05 Jun 2024 13:58:43 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json
