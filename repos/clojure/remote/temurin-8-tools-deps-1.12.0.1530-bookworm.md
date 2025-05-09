## `clojure:temurin-8-tools-deps-1.12.0.1530-bookworm`

```console
$ docker pull clojure@sha256:475a9803a049314e7f687133d7936babff5b6a1617480929c9f005cdda92eee5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.0.1530-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:3bcfcb71a8cf42c0d0d01564ffa17a98bc87f0540cf3f1c492d6c9d54fca8785
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.2 MB (184199710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac69e73aed59516833772b19614c794145386b8ea931c143bdecdd1a55feec3a`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:cf05a52c02353f0b2b6f9be0549ac916c3fb1dc8d4bacd405eac7f28562ec9f2`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacc64f2150caab5b2e18c4de086d68be10cecd36b2a46e72d0fd9a77dcb61b0`  
		Last Modified: Fri, 09 May 2025 12:38:58 GMT  
		Size: 54.7 MB (54716197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc271d35300eea5fde26d13a46aaaed6aa099ea8860898a4507e110febc1968f`  
		Last Modified: Fri, 09 May 2025 12:39:00 GMT  
		Size: 81.0 MB (80991670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a79eb33df71146d25d3f922dc8af7b245dd9449c884c1dcfe572c7aeea3029`  
		Last Modified: Fri, 09 May 2025 12:38:51 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1530-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:5f7a20b7fd1756ecb143103f44c51efa38a68da20f1583ee86c66227e456c000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7308323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8275c7745783c98d9cf9f6f3752ee89ae42a677b6cca8a47ca22e938427ac8ab`

```dockerfile
```

-	Layers:
	-	`sha256:be2e64348a2a86c660a559e86788cb5450c9dd081599f152204a3dc5731bf258`  
		Last Modified: Mon, 05 May 2025 17:07:03 GMT  
		Size: 7.3 MB (7294086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97b28a0f4c8bca4852ae33fc92a4b4744c4993d944ecc412274d07920167fe47`  
		Last Modified: Mon, 05 May 2025 17:07:02 GMT  
		Size: 14.2 KB (14237 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.0.1530-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fa7b4e9b69bb36a6b0b82203a26684865c2d5064cef9753a2341e9f5682885cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.0 MB (183002764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69d777395c807ceb0731a37946998706bab6db376f9bceefc96a6a40521d4e2e`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:de07ba6f486e0ce29760ab32d4381edabbc660a04c493e95eb9a8056925d8955`  
		Last Modified: Thu, 08 May 2025 17:04:44 GMT  
		Size: 48.3 MB (48327644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a4ac50ae12613ea163dbff6882aed70ba62bcd9958c1353461920336c08460`  
		Last Modified: Wed, 30 Apr 2025 00:58:35 GMT  
		Size: 53.8 MB (53830497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdab30ec3520d7158eaa6d2866bfb67e85b7e9b1529858351fa3d3bd39c56a89`  
		Last Modified: Wed, 30 Apr 2025 01:01:39 GMT  
		Size: 80.8 MB (80843980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5edc077c7df0c0be13ca86b97e1a3e14c68e740fb97b099c42a4932a2bfc2c1b`  
		Last Modified: Wed, 30 Apr 2025 01:01:36 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1530-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b9cc36266b0be4a7b5a32eadb6a524c72608c873d36cccaba2804de64415684a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7314902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8fb58253c88916390ca4d63d5809168a74f896fd93cd2a9a58f9721d6163075`

```dockerfile
```

-	Layers:
	-	`sha256:f7d87b0964995f99148cd61ee4ffc0c9b0242b2b6490d5023c9c422ce88c0349`  
		Last Modified: Tue, 06 May 2025 00:19:38 GMT  
		Size: 7.3 MB (7300547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d36d0d9de6a0757034da4a98b42a38ba043b58bfe52f7288ec8f64bff58a7ba`  
		Last Modified: Tue, 06 May 2025 00:19:38 GMT  
		Size: 14.4 KB (14355 bytes)  
		MIME: application/vnd.in-toto+json
