## `clojure:temurin-8-bullseye`

```console
$ docker pull clojure@sha256:6f36b326aafcb2637b72319aab0edf06f0c831d2bef83c129fae7ade20a73dc4
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
$ docker pull clojure@sha256:2ab2ce23427f447bf43cec9e6b656676d2e91f20694daeb3c08d36f9328f7bb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.6 MB (175620940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0d344521d70aa25383ded0f16c2aaa46f36cd01630066d784dce9a8aeeb2fa6`
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
	-	`sha256:88918068b7585dab0070378f127b0caf694182f270e60353faa57f3f33bcdf64`  
		Last Modified: Wed, 02 Jul 2025 12:06:33 GMT  
		Size: 53.8 MB (53830515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:997f619931f5cd3776b1427e1427dec07fd2061a93402732029a586564a5857b`  
		Last Modified: Wed, 02 Jul 2025 12:12:39 GMT  
		Size: 69.5 MB (69537528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f50d4f7312c87c1d0b55160fcef13d4e6d9f0f1be8cf6019d589bcf136a87b`  
		Last Modified: Wed, 02 Jul 2025 12:12:27 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:a320913a0d5c75e8bf1baf3256814f9209418c66e54c10cfcd9344410efd770d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7537400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c700f3727914b82adc6c776d39f79634825e05ba238510cda04d5e931f1bd95c`

```dockerfile
```

-	Layers:
	-	`sha256:0304e326192ad22f75ac4994417e619ccb14a4991870cb35bad033f43dcf4e0f`  
		Last Modified: Wed, 02 Jul 2025 15:44:18 GMT  
		Size: 7.5 MB (7523045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d97dbb1e092792d96a90b97811dc804b834da222081e6de3c6db136de21e9731`  
		Last Modified: Wed, 02 Jul 2025 15:44:19 GMT  
		Size: 14.4 KB (14355 bytes)  
		MIME: application/vnd.in-toto+json
