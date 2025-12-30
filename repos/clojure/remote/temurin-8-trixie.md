## `clojure:temurin-8-trixie`

```console
$ docker pull clojure@sha256:286eb37f79d17d300c86c2a99fbaf3cf7531e99f068ba2d744bf76b6d7d12b62
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:78d39db0245f4bd44febf5cb5ed8eaf05e35f2c3f103d96b7a500f5223c2b38a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.6 MB (189566479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ec13e4805557951964d65b5462ec0cd6f005eeff4c8f6ff7f417d3dd2793ab`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:52:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 00:52:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 00:52:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:52:08 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 00:52:08 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 00:52:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 00:52:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 00:52:25 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:281b80c799ded5b9a390d2e8c59930db01ee395ab809dd34259897c660751f4e`  
		Last Modified: Mon, 29 Dec 2025 22:31:07 GMT  
		Size: 49.3 MB (49289587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696ccae2a6ee67ba4e79048983fd446dbfd9c638606b13cfa1c9cee54d748a83`  
		Last Modified: Tue, 30 Dec 2025 01:05:51 GMT  
		Size: 54.7 MB (54733371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14151e174a722d9002c9998fb1436022619d9ae18d1a6fbbdc7571108df6a8f`  
		Last Modified: Tue, 30 Dec 2025 00:53:02 GMT  
		Size: 85.5 MB (85542877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5bc0772b4f87fe787eb5214310f364432e6a9a95abb54fc0b881f78c814fbaa`  
		Last Modified: Tue, 30 Dec 2025 00:52:49 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:957bbed00aae28cdea44687b7bef81a07883f92e6916d7ac147af66d7f120b46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7602709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf65ff1534c8cc53824318f39c4efba6c12e4e38ccb67a6f8f95d5d550539970`

```dockerfile
```

-	Layers:
	-	`sha256:d42913c3f9f8e62884c65f67ae70a4acbce3c15f65786ce8bf69bd877d81794d`  
		Last Modified: Tue, 30 Dec 2025 04:50:03 GMT  
		Size: 7.6 MB (7588539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2ee140d81ad29592ea2346d85c8fe6d3b3642932fa13857fb9bd9efd843a6c2`  
		Last Modified: Tue, 30 Dec 2025 04:50:04 GMT  
		Size: 14.2 KB (14170 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:31c09e10c66383d1ba17e7db38b1244fb2945823762e8169c8a5d963c2660760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.8 MB (188827181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3289c831111f19f3e132b10a8c4920c1c3795465d752a03aab7945fd90c7698b`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:54:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 00:54:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 00:54:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:54:37 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 00:54:37 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 00:56:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 00:56:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 00:56:00 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:5785abec2864dcd8d343ccd872458a50ffb2a61739bc46a79709c68c455cb8fc`  
		Last Modified: Mon, 29 Dec 2025 22:30:57 GMT  
		Size: 49.7 MB (49650193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95a66de7f356fa76988e9ebe5975965d77910619e719aa96b3f18bbc6a94abb2`  
		Last Modified: Tue, 30 Dec 2025 00:55:21 GMT  
		Size: 53.8 MB (53814992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aec2e0a5c8f0cbcfaabdb6b9bb3200a9ad4a31f6cc9e3fefb78fd574d839e09`  
		Last Modified: Tue, 30 Dec 2025 00:56:38 GMT  
		Size: 85.4 MB (85361353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d037e74a0a39a6ebadb3496a87e29e7940dad7b08f84cdd1325ed97b62884a7`  
		Last Modified: Tue, 30 Dec 2025 00:56:23 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a9f6cc503747c9f9da9a0341de3083997b6d93314d9ff8eba8226ba2e257a448
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7610554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33c1e513a4c205422f9137c1e62d2dde9c48d8eff5b769b4bf8d05a43df96cda`

```dockerfile
```

-	Layers:
	-	`sha256:fca3c3ed70c629c9ecf41b77751f950b604e4a7f3c7e21545530de832caa15f8`  
		Last Modified: Tue, 30 Dec 2025 04:50:10 GMT  
		Size: 7.6 MB (7596267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1da6f6433cb29b82ab33c7fea8cb1ddfac911d600fb5e568eef38c839adc6bf7`  
		Last Modified: Tue, 30 Dec 2025 04:50:11 GMT  
		Size: 14.3 KB (14287 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:f3626535c047d88563504ec15401b3f71de99d8cff01e1a0d8d2c0c5eef76dd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.2 MB (196229266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63ae6f6f727821bc6eac46645c7b75927041147616b3816933f44208c01160e7`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 05:12:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 05:12:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 05:12:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 05:12:24 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 05:12:24 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 05:14:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 05:14:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 05:14:59 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d586c84fb9377f9b3f4030e2c3e1e9ff7b1a23a68b8abc2c48a43163a3589257`  
		Last Modified: Tue, 30 Dec 2025 01:51:01 GMT  
		Size: 53.1 MB (53108485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712597973b595c19402df1e5710d5565c7fa6467f856fa606197ec1e7e8a4aed`  
		Last Modified: Tue, 30 Dec 2025 05:14:21 GMT  
		Size: 52.2 MB (52175123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313c085eaae9c7b40fbcd46d3a5c2f385e92c6c74552beb7fb6bca30f78b7cfe`  
		Last Modified: Tue, 30 Dec 2025 05:15:51 GMT  
		Size: 90.9 MB (90945012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70229df2fc160801a8e03d46893c4a3d1185510945eafcb65bf36da929bffe84`  
		Last Modified: Tue, 30 Dec 2025 05:15:45 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:5cb42f89b5eebc568d01fe5fd1bd3f6a60afa91bfb2612cf243e01b693b28b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7607768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:115bf4e2c0c71e7f8d04701ef8e66402b2518d70d77dba9428bed7bbf33bb485`

```dockerfile
```

-	Layers:
	-	`sha256:49a8a20354870d819ba24e0d51972e2c58f661b075d60f164d1c8649280b408b`  
		Last Modified: Tue, 30 Dec 2025 07:40:16 GMT  
		Size: 7.6 MB (7593551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ce3698549e7c5ac091d7285e2bcb672f5cd3e3945f98f042e643f8e93e9904d`  
		Last Modified: Tue, 30 Dec 2025 07:40:17 GMT  
		Size: 14.2 KB (14217 bytes)  
		MIME: application/vnd.in-toto+json
