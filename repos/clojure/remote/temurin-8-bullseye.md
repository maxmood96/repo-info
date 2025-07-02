## `clojure:temurin-8-bullseye`

```console
$ docker pull clojure@sha256:1ad605fb003fb93a249eb203123c7f0de1b6bb7dbd135fe1275c582fad96da33
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:7169fb9b1681e518b8e01350878d6c058ec51b92f2965e3e5091aff214410cce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.9 MB (177881512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e3321b1c705dd7c5f275d0ab098f09a99ba1a5ef04120b0ccd213af7fafb38`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
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
	-	`sha256:2d765646d883a37610a09973a079fbba4c7596e54d18d0447bdfff142389d1f7`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 53.8 MB (53754822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d8c706fc7387e9e86e9003ca5b107ede28fe7432d3eb5891487af2b464bd96`  
		Last Modified: Wed, 02 Jul 2025 04:15:50 GMT  
		Size: 54.7 MB (54716192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de84c5e10cab62d350e32d3f67d317a1248d9747c337f13d87cddcc7aff8b7b7`  
		Last Modified: Wed, 02 Jul 2025 04:15:53 GMT  
		Size: 69.4 MB (69409855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fef7c355570a608875453e41697dc932f58627be3309612fb9026ff1e38d79d`  
		Last Modified: Wed, 02 Jul 2025 04:15:52 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:4d69355c300f0982d53951341b3600858c98bab9d64968ab68386b2627528795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7531485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ba296e3f54f4bc65952f2e189c1c26269cb450feb651240c88fec3d70019d1`

```dockerfile
```

-	Layers:
	-	`sha256:fd76a4ef1a3a94a65380e76f204d4b3d2ded50ed450aea8e6824dc1e99aa1123`  
		Last Modified: Wed, 02 Jul 2025 06:43:04 GMT  
		Size: 7.5 MB (7517248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5cdce4d1415230a883212fe0b436fe06e1880182d65582f13044d7f681aa21f`  
		Last Modified: Wed, 02 Jul 2025 06:43:05 GMT  
		Size: 14.2 KB (14237 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:983de7e3b5117170276b59dd28eb7c037455e3ba91c0e131e795d081d7a277a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.6 MB (175620893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44702d5904e78d42c73d9ffbae775f095bc834502b16f326dcfb87ec1e3f5394`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
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
	-	`sha256:df45b4853b6fce6b81d1ac6218d861c6d7c8c14da4be409d42ee4bfdf0737e71`  
		Last Modified: Tue, 01 Jul 2025 01:15:18 GMT  
		Size: 52.3 MB (52252254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2173dace57cd95f6b961f519b1831f8dc02594b745e5fa3f8192bc4de9f28be3`  
		Last Modified: Tue, 01 Jul 2025 11:57:44 GMT  
		Size: 53.8 MB (53830497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4b041a3f8343ff45f280c19af39f36ebba4cf3131ece43b5d5861ed9fb277d`  
		Last Modified: Tue, 01 Jul 2025 12:02:30 GMT  
		Size: 69.5 MB (69537500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd0743695a959fd4d850d6708ea93f9d00ace096f77607c3e81460dc8f64389`  
		Last Modified: Tue, 01 Jul 2025 12:02:27 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:e8f1fe5a7d2076d4dd1f89af0ecf6132430cfae81cbc37736971a40b23334154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7537400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e884fadd88dd099b5bcf3b89e9ffc5770e530b87ccefb40f0f57ed573f1c926`

```dockerfile
```

-	Layers:
	-	`sha256:c20f0594c6a838e0ef7869ab20b5dd4cf5a76ed0ac7a55eb722f2efee85eb869`  
		Last Modified: Tue, 01 Jul 2025 12:38:50 GMT  
		Size: 7.5 MB (7523045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a154584ddeaf9f6096c8a6084e31369650d87e1da8cfa87d9cef2392f384135`  
		Last Modified: Tue, 01 Jul 2025 12:38:51 GMT  
		Size: 14.4 KB (14355 bytes)  
		MIME: application/vnd.in-toto+json
