## `clojure:temurin-11-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:a851d8b03ef858a43f8d04a8208462ec53b155f6c91f8126537657102599e216
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:148f101703e670c001328e30e0c1b08270e630e5b8f54cc9cfe16c200bccf33d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234886428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:882317e948726f6918bfe19270c31567dac0df46dc36ea8e1db0c3e5735af274`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Wed, 21 May 2025 22:28:05 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d422aaca88411f296f86121286899d79d1fcbc7e3c0a5a8f16372016a229ce8`  
		Last Modified: Wed, 21 May 2025 23:32:32 GMT  
		Size: 145.6 MB (145635749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34d6f0101203676af372160ac8f5e476f210e183f73095c2fec22725d8a823a`  
		Last Modified: Wed, 21 May 2025 23:32:31 GMT  
		Size: 59.0 MB (58994096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5120ad018485f00f27767355335a60f6ff41ded6efd5b0bb69475718989a3f72`  
		Last Modified: Wed, 21 May 2025 23:32:30 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fa0a4549719fdec1777f4780c65bf32d0ff0237a71e6f394369d21dab4d7e711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5201441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5756ef0ed364eb35e06037bb1d7d9bc223e5f5573bcd9f4c249e9a5d4e32ab2`

```dockerfile
```

-	Layers:
	-	`sha256:46c183bc2128ef212b00e933d55541741fdb5da8b3840ff93db6f414ff9d4590`  
		Last Modified: Wed, 21 May 2025 23:32:30 GMT  
		Size: 5.2 MB (5187131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbe06d214b997abff9b430bbd572af6bff3b81d50a2e757e963f66b845bc6a99`  
		Last Modified: Wed, 21 May 2025 23:32:30 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c5189c8117fe049a57b9c8b8b460ca562243c4707d40d01eb7ef4c53d552e51f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.3 MB (230293588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fe23693246ade0be2b8fe6f715dd3e19ec7c0e000d987061d1839ca5f77c4a3`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:5d3a81360c5bb9281a4f735a1468429a1898f1a4fc24a2581dde4cf28ace4488`  
		Last Modified: Mon, 28 Apr 2025 21:21:09 GMT  
		Size: 28.7 MB (28744645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b561ac98db1022e14acafebccf18d2e70cfb7fd976f4944169fc6db0567635`  
		Last Modified: Mon, 05 May 2025 22:05:58 GMT  
		Size: 142.4 MB (142420730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c43da759ade31cf93b18b1e9e39a99a6d12ed474db0d4c2cb283d4476e422dae`  
		Last Modified: Tue, 06 May 2025 00:30:08 GMT  
		Size: 59.1 MB (59127567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:effec24006f3e6788a58180d2c977f5a4b7fd869939e42724e9a2ff8ba3b2b5c`  
		Last Modified: Tue, 06 May 2025 00:30:06 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b604da0a6380ddeddf74bb45855d8a660090d2a76dc7960d928f2f9a7713d8e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5159986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b7c0874aacfd3a675932ada4a9846e47bb0746e56c147deffda67bf10c69a1`

```dockerfile
```

-	Layers:
	-	`sha256:984c6e28be1e8f6bdbef83a545cb152ea9d8ea534925e22d219ad63e3b847c9b`  
		Last Modified: Tue, 06 May 2025 00:30:06 GMT  
		Size: 5.1 MB (5145558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be412bbab0d30fe9842e04e0410dce380bec269d66a90250142132204069ef6a`  
		Last Modified: Tue, 06 May 2025 00:30:06 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json
