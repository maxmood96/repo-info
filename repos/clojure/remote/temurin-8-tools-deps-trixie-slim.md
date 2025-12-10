## `clojure:temurin-8-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:3d4472b43a7a77b29dc6e59d86fca346752964a3bb63b3c6f327baf813d73aee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0e1f44dd374779079196c37319c41bb82737b3b9ee0708ccb036748237b6d643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156506523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d0291be24180fbbb78676f81de8002dea7693beb8245dcc55f1eb5b3bd6b2c`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:50:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:50:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:50:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:50:24 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 08 Dec 2025 23:50:24 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:50:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 08 Dec 2025 23:50:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 08 Dec 2025 23:50:40 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb392fcd0bced9416ef81d8e77a3db0723a27c44865790b81df81caa8ee115b`  
		Last Modified: Mon, 08 Dec 2025 23:51:11 GMT  
		Size: 54.7 MB (54733371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a19207e261dadff9c5e9005a96222a6d3233c8461730943fbacd6722708550a3`  
		Last Modified: Mon, 08 Dec 2025 23:51:12 GMT  
		Size: 72.0 MB (71996013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422d3ca6c57641e7fca7aca224a43893a55995b24e7a28da7b8ac8a7cf170dc1`  
		Last Modified: Mon, 08 Dec 2025 23:51:05 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:75b8369bfbc2a24136699b77560867cb624d0290f811b74959a4148b10c3a611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5392035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14e9011dff74f8e8dec5f3066c53af34a9bf902fe3b5c1b3b3121c203865cba5`

```dockerfile
```

-	Layers:
	-	`sha256:c55698a058a8a87d28e16426637df93f31a92b9470c82a45f8fa593c0474035b`  
		Last Modified: Tue, 09 Dec 2025 04:49:47 GMT  
		Size: 5.4 MB (5377807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad38a1d3b1d9f1dc6e4dd91c02ab4601176e0de9686bffdb8e65fa03b1af5e79`  
		Last Modified: Tue, 09 Dec 2025 04:49:48 GMT  
		Size: 14.2 KB (14228 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:62700357db9c985fc9f6023003972fc55cedf9ca12ed580c7898cbb1ce8bdcd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.8 MB (155762828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:905151ed30806fd4ffd792e642d9d6f0137b95ef5aa1d9f3e47ac9f29de772a3`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:58:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:58:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:58:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:58:52 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 08 Dec 2025 23:58:52 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:59:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 08 Dec 2025 23:59:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 08 Dec 2025 23:59:10 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf202aaf71ccca8808e83d5afcdf335b96388e161a5ea699b53fe0243ebf78bb`  
		Last Modified: Mon, 08 Dec 2025 23:59:38 GMT  
		Size: 53.8 MB (53814993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b45e68417d604c6b290bd8b15c299d7fa7e1b603f6fcafdd0ff3380bf531f57`  
		Last Modified: Mon, 08 Dec 2025 23:59:45 GMT  
		Size: 71.8 MB (71808563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607b01ef1bd861cadd7417015e4ef947c1c3136446f90ffb82161cb4c7618b38`  
		Last Modified: Mon, 08 Dec 2025 23:59:32 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8221b0e9e12aa4f184e0307a398c76366cde5d76a95d3f2cf5cf7f43ff6197b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32cb079c10e4969ce7cbfa4de416bc5c4cc4187076100418565b01784e542817`

```dockerfile
```

-	Layers:
	-	`sha256:6dc765fb3ca1449f82f919157eb68979b2a413123e71a0cb8d80a3fcebbbbb31`  
		Last Modified: Tue, 09 Dec 2025 04:49:53 GMT  
		Size: 5.4 MB (5384274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad8415ff19feae99b6d4bf9de7f4069d03a3d1adaa06d183632e601f86833870`  
		Last Modified: Tue, 09 Dec 2025 04:49:54 GMT  
		Size: 14.3 KB (14344 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:5190e4034750bb8140c1d12f0dff5be3c044d8ae1b2fc13484cb466f3b570159
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.2 MB (163163498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ff0abbb9a69c100047b7b7950ca73509600348348a374c5d098b043653f2c4e`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 03:46:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 03:46:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 03:46:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 03:46:38 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 09 Dec 2025 03:46:39 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 03:49:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 09 Dec 2025 03:49:27 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 09 Dec 2025 03:49:27 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9ec5d91b1da27248b6474c55829b4ad5637900f96134ea7cb65096baa6ecbc`  
		Last Modified: Tue, 09 Dec 2025 03:48:24 GMT  
		Size: 52.2 MB (52175138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89eec25bcb0a1f5d9d931471a239db442a92e890da000ad099ec0b532260d3e8`  
		Last Modified: Tue, 09 Dec 2025 03:50:18 GMT  
		Size: 77.4 MB (77390825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a512634141b6758bd9a0cac5161d131b55204417e978b92083a89d1c2e57e4`  
		Last Modified: Tue, 09 Dec 2025 03:50:10 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ef8f24ad656bd0aa4448df12c183e2d83f5130cc7d4b08009c0a2fb6efd5b7b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35da74fb37ffae8e73f8027d35599f6d82e84006a4eb91106966e9da7f015e2e`

```dockerfile
```

-	Layers:
	-	`sha256:4ea87518ea6bfc6def3310f4d12bb5a72c7dc8e9c6bf87957bb6940c34d6faa9`  
		Last Modified: Tue, 09 Dec 2025 04:49:59 GMT  
		Size: 5.4 MB (5382771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec5bb8b379d79e8ee6ab09ad8ee6310ca5ab5aef812845e9d5f6117df6371f23`  
		Last Modified: Tue, 09 Dec 2025 04:49:59 GMT  
		Size: 14.3 KB (14276 bytes)  
		MIME: application/vnd.in-toto+json
