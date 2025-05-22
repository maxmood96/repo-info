## `clojure:temurin-11-tools-deps-1.12.0.1530-bullseye-slim`

```console
$ docker pull clojure@sha256:db01ae001927ca4ebb3065c4264e1c19563690d5cf587846db8c76c0366c045c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.0.1530-bullseye-slim` - linux; amd64

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

### `clojure:temurin-11-tools-deps-1.12.0.1530-bullseye-slim` - unknown; unknown

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

### `clojure:temurin-11-tools-deps-1.12.0.1530-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3c5cdc51504ab685ec9f2d86b0af18617298458126e94bd45d4c9eb5be28567a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.3 MB (230296663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c713c38f8b6c1fe4eef97da34ed9f7733cec5e1e34a8cb5f15e579c3f72dcb0`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
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
	-	`sha256:66850c8b65c1e9c3674a722b71f8887dd317a9b257148bb1063e88d85790544f`  
		Last Modified: Wed, 21 May 2025 22:28:28 GMT  
		Size: 28.7 MB (28746257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4089ffb1a4dff6639b70fa34d83a369967ffca2c451e73ba59edfdf735eb232b`  
		Last Modified: Thu, 22 May 2025 03:17:39 GMT  
		Size: 142.4 MB (142420720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ae7b68c1876f8d0c354fbea2536f9d8ea7c42c37a9222d5c50ae618b707891`  
		Last Modified: Thu, 22 May 2025 08:16:36 GMT  
		Size: 59.1 MB (59129041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd493c5cf1997f3ec3b9b76d3765064435a3d494a284cde9a8447d6dde421a2`  
		Last Modified: Thu, 22 May 2025 08:16:34 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1530-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:35cc945163916b7c56ac49bf2ed039a0e3036f2a4943ad1bbb7039a8502bc1b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5207908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8512a04abb45963a48516911a508f222f5ddbc9de55610f4c5efc2b45f0ea2c`

```dockerfile
```

-	Layers:
	-	`sha256:05c06709d817427368ce3b0b26233487a908c4f4c74abfaceddaac4c9e29bd6b`  
		Last Modified: Thu, 22 May 2025 08:16:34 GMT  
		Size: 5.2 MB (5193481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c562b3e2eab01ea260ae8a4db365cd77745d4ec50cd9a0191962c1dd933ebe7b`  
		Last Modified: Thu, 22 May 2025 08:16:34 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json
