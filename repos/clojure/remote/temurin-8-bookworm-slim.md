## `clojure:temurin-8-bookworm-slim`

```console
$ docker pull clojure@sha256:4f0d71347529000ae060edc728d0899b4959890835d15c62a2f60d77d764487d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ecc766eaba1d4d14aa85435d5ac3d7362b4b115eb23dd7767ac95898e4b8dbec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152470105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b934b507767bf34776cf10051c42ea594232915b18b1a51187c72940f61f115e`
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
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Thu, 08 May 2025 17:04:38 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59d89cf3c4d59d95710ee429f2dbbacd4f66a8107d3506ca30726b890163ff9`  
		Last Modified: Fri, 09 May 2025 12:36:45 GMT  
		Size: 54.7 MB (54716178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991425c87aa3891dafefcf513a559136080fde12e0f04111ec4370ad2b130e91`  
		Last Modified: Fri, 09 May 2025 12:38:33 GMT  
		Size: 69.5 MB (69525641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f020e71298a0ada62f7ccb180f0c13d340a42a975952468a91aa2173cf63c5e4`  
		Last Modified: Fri, 09 May 2025 12:38:27 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:36c16947aac441297c4e4fd5b50ce7b97ab3789a93c8837a22d97f34f2c5d808
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5049866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b151d300c755208de1f01fe1bf9010b423e8fb5ba1abb9e040b7e4752ea04c2`

```dockerfile
```

-	Layers:
	-	`sha256:09b078da492d04fe53d5ed25703b474fae41c3dcfa3e36f4ce660e1a7f6f06e1`  
		Last Modified: Mon, 05 May 2025 17:06:53 GMT  
		Size: 5.0 MB (5035575 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af95a26e4acd11b8f9619bde6e7925b1894f3eb193d8c89cacf5e6cafe317e44`  
		Last Modified: Mon, 05 May 2025 17:06:52 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a2680f5183bacea3a5960b1bf488020bdc9fbfda709562067f6bcd97a3f3c7a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151275459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6d04fa5d140509a9396ae5676da51a546c16d87988d38f2a83118a1b029da9b`
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
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95561fee27ec3c57c777d90b1887be2a2e08f63416624593b6fb5e2e09b86a98`  
		Last Modified: Tue, 13 May 2025 19:21:19 GMT  
		Size: 53.8 MB (53830490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd06b14693cca080aa7fb6f128b81a663c30ec1667a691ef0e21c259af0697e`  
		Last Modified: Wed, 30 Apr 2025 01:02:19 GMT  
		Size: 69.4 MB (69377703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa49988e737c9b485e2841cbd6b5d8c789144e9a4198f1c7949f75c78644f64`  
		Last Modified: Wed, 30 Apr 2025 01:02:17 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9e0869e3cc56be7fcc703983674891619a6d3de5620973997f0784adc2ed4c48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5056443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:701666f31aa933fab6a93fe6b6f66a3809ad8d57ef60a58c5ff303ba9125782a`

```dockerfile
```

-	Layers:
	-	`sha256:a8296b4ee5c5ee1e4f975dc7bbf04bf8675036118530670c2a61b14859306431`  
		Last Modified: Tue, 06 May 2025 00:20:01 GMT  
		Size: 5.0 MB (5042034 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83bc91a30c6c66010e6d28a2c8d5a44bd7f7fbe85e555957ef92db8816a7621e`  
		Last Modified: Tue, 06 May 2025 00:20:00 GMT  
		Size: 14.4 KB (14409 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:1de6e0fff50674d58066d5b5ea4c5371d41009184a2459cb687769339c34c6a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.6 MB (159581961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131fdb0585ae193d0ae52b840b9c0252165bab7b4297901ea926adbb24dc5f68`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
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
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Thu, 08 May 2025 17:09:00 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0ff21f998b476820ba3e6b42f7da8947c75145e9bf234605cfece8ce02148d`  
		Last Modified: Tue, 13 May 2025 17:58:46 GMT  
		Size: 52.2 MB (52167960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4acd74618dca3940b6aa6c14da546195bff6670502730f6412720a01d976118`  
		Last Modified: Tue, 13 May 2025 18:10:40 GMT  
		Size: 75.3 MB (75344912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dffe7529890448cedc121fda2507114b5eba8c2a5c59c8cd09024e9d9cfa8104`  
		Last Modified: Tue, 13 May 2025 18:10:34 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:869a0117421c0c5e1f3a8e0fe9a476a0fbd154e15a464a327b0edc5fc10d1f82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5055499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:975047c4f68d05bb8d5c1fe1ff7fbf89579aaed5882d6aa61df1badcfc918a41`

```dockerfile
```

-	Layers:
	-	`sha256:9487b08d26455ea3d417ab1d9a7d0f9d5acb653cab429e020e147c0da2f57e79`  
		Last Modified: Tue, 13 May 2025 18:10:35 GMT  
		Size: 5.0 MB (5041160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41fba4dd4794cfdb50aeb3f0c0cbee6b186515b983c563a5d1457e65a44d49f1`  
		Last Modified: Tue, 13 May 2025 18:10:34 GMT  
		Size: 14.3 KB (14339 bytes)  
		MIME: application/vnd.in-toto+json
