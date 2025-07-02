## `clojure:temurin-8-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:0cfb755dda5394c762ef8e9e677c20efe3912d1a275b03e2c35918501e993ee4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:9ff0b1db95c8b727d30ebef22a77ae89058a4f06701954e5a9da8e67e5768f1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152480122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07185b6745e1d4450b50debb726592f08dbd03eb3a4b244e55cf00b36fe1adbf`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
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
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee67e87bc34a283d13189c69f6915f6d99b1b6d195c83b2a572dd211d08593a8`  
		Last Modified: Wed, 02 Jul 2025 04:15:50 GMT  
		Size: 54.7 MB (54716197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9feb87dc4ca32c04c9a2c4a540843099939e595e18e5f550df3956dd0118db02`  
		Last Modified: Wed, 02 Jul 2025 04:15:50 GMT  
		Size: 69.5 MB (69533139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f3e61995e1e1b16eb5a32727afd515a4cc804e5bd96dee7e486d9aef774eecb`  
		Last Modified: Wed, 02 Jul 2025 05:44:09 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c7077ee3b24bf82f43b8cfccee6b348f58202f805620192a92919e18ebca3080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5247145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8090bb4a58b06d4609e4671dcc9b9bfbf62258bcfa44b4f5586031c1696f188`

```dockerfile
```

-	Layers:
	-	`sha256:c3caa5090e08754bf7d3dd65ec902c7ad642e9b91b0de6689ba1001af6cf0934`  
		Last Modified: Wed, 02 Jul 2025 06:42:56 GMT  
		Size: 5.2 MB (5232854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55bb3806842bad35d075b537000b392dd0af1a3e362b5d3cca153fdd60a356db`  
		Last Modified: Wed, 02 Jul 2025 06:42:57 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f029d4bdab68c54eb969bbe6a7e0aa9f65387d524387227ea97dff03ec409640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151297441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4fe9c1b587188d5eecf4d6a9ff050573864f7b5470eface4e23a8af19d63b5c`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
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
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c679baa0c56e50c43f0884e8844d0fbb7c9898866aa0b1eddbc7c174c0a53b`  
		Last Modified: Tue, 01 Jul 2025 13:20:49 GMT  
		Size: 53.8 MB (53830509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5bbf3e84c56b067405ee1153cb319c6bda7cb8707c4e64bbc0959e6dcc7697`  
		Last Modified: Tue, 01 Jul 2025 12:01:57 GMT  
		Size: 69.4 MB (69388609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f3984be063b2c20c6e5d5d94aadb8d51adc643b0bee7d57b6328bec81865bb8`  
		Last Modified: Tue, 01 Jul 2025 12:01:54 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b9cb78650cfac728c0f44fe69c1223b469e8c85ea441305b57ac7a9d4d331c37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5253722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ca52cacc0ddc58b084286620abd5a3d609fb902c1a10e2c4a46db79025e34c0`

```dockerfile
```

-	Layers:
	-	`sha256:9643062f870d88264ad77d8b855e6917d3ddb56cc33180b0ef4ccc4e9aa48231`  
		Last Modified: Tue, 01 Jul 2025 12:38:44 GMT  
		Size: 5.2 MB (5239313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e9ba82e8da46d99ff5dd95b4ebe6b79aefd657a2ff3103f5dbf191a4f6d24a2`  
		Last Modified: Tue, 01 Jul 2025 12:38:44 GMT  
		Size: 14.4 KB (14409 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:24eaa63875ab17f78df1bd5877106867aaca6dcc1b3206aff374f879cdcdd3c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.6 MB (159598921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5748322925374953be130a13979428cd8381dcbcc4aee09e7f17763c2101b736`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
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
	-	`sha256:c5884d20b08634214a92bd5de559876bf30e6c5453807c3014f5480eeba20662`  
		Last Modified: Tue, 01 Jul 2025 01:15:20 GMT  
		Size: 32.1 MB (32072820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6893361e922cb321182c5a6404c2c6bfb11da610b3e5d97b0f1485c9c7d814cc`  
		Last Modified: Wed, 02 Jul 2025 09:53:07 GMT  
		Size: 52.2 MB (52167961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d53a81bcca4099a0b43cadeaca239148e4dfcc302c4dab859f29ce5d1469f4`  
		Last Modified: Wed, 02 Jul 2025 10:02:45 GMT  
		Size: 75.4 MB (75357497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7fec0363db6dcc90aba1ab90164f54b0217589b7524bebf2ffb72d762569bb`  
		Last Modified: Wed, 02 Jul 2025 10:02:19 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9dacf915ba19afc5f8b8e414f4c36dde0510afe1cc4f41286ebe607ff38fa23e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5252944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f90315a2dd15f077524ed21711a213e8063df7411b034e802b5d9009058668f`

```dockerfile
```

-	Layers:
	-	`sha256:da4100834569f8bd47cbf1ca3754e594e3fbe8c572e6f85e246444a562f52204`  
		Last Modified: Wed, 02 Jul 2025 12:41:28 GMT  
		Size: 5.2 MB (5238605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09b29ad02b1db5a1ed1ee1e9141825ee708ef5ac5e663f73a791cb6e1d00de3e`  
		Last Modified: Wed, 02 Jul 2025 12:41:29 GMT  
		Size: 14.3 KB (14339 bytes)  
		MIME: application/vnd.in-toto+json
