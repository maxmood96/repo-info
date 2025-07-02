## `clojure:temurin-11-tools-deps-1.12.1.1550-bullseye`

```console
$ docker pull clojure@sha256:85b5e6f9fb5f92243bd554f8a06226aea3760da2549044e56593ccd08982c333
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.1.1550-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:318d4945b5d004b7dd69f5c596753860815530347e2f5c5dbeaefee57c65a3dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.8 MB (268801051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fa4326ac34c43e1828f2a89398b5e1b5372fa67242a7fcdae6732b488a56798`
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
	-	`sha256:0842356543045cb30572363d8c4cff5b1b614375fd83098d67c9a9da2391b507`  
		Last Modified: Wed, 02 Jul 2025 17:11:52 GMT  
		Size: 145.6 MB (145635777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a819ea69b3faa8006b2a02dab4d4be9d8f07d4df0d9a1c7de8ebc5add8bea111`  
		Last Modified: Wed, 02 Jul 2025 17:11:43 GMT  
		Size: 69.4 MB (69409806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724ae3c783771b9085da4a767271b367c19a186bb9ac4db865c4f1aadbe4edf0`  
		Last Modified: Wed, 02 Jul 2025 17:11:42 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1550-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:5887f74c336fdc64f88712cfee7908dc92b375783e4b1e1192a343dc39451cac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7430031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f248eb87b711a635351deba4e2600b14f50f5bba1dccf94b1c533db566d5afaf`

```dockerfile
```

-	Layers:
	-	`sha256:0f0b604dd720d3d018a15e0ddd9b247a63f6e20e136aaaaea257cc3985d7c131`  
		Last Modified: Wed, 02 Jul 2025 06:35:14 GMT  
		Size: 7.4 MB (7415779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:036c170fcbff21686eb11e5a528238b1296fc46eda070acbae4fa042ec2fbef0`  
		Last Modified: Wed, 02 Jul 2025 06:35:15 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.1.1550-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:312d414be00828ef8527c6715c42590d0d2cdc72d2f20941cee76f1dfa54fbb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.2 MB (264211215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eddce10c8ddda7aa3db50d96f445d27237983a873910a4183a7145e6849520cc`
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
	-	`sha256:8d18d0c94acb88248800b86b1188c3cc4a74927b3309f5670e543bf8f184ee07`  
		Last Modified: Wed, 02 Jul 2025 17:12:44 GMT  
		Size: 142.4 MB (142420701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b3412d1ca0f8d189bbae33fdf229b897a23e3bb11f879ed5bf7aab89adedf4`  
		Last Modified: Wed, 02 Jul 2025 17:12:40 GMT  
		Size: 69.5 MB (69537615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9103c2520aff01777ac91713be201d69f7b07c386482724b7801833ac726a0ce`  
		Last Modified: Wed, 02 Jul 2025 12:24:56 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1550-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:f874af7663d687fd245c91926be9fbeb0f8649974a227dc8d0b1fffd0b2ab5f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7435866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f681687b7c7d57053bf132ad7b798dde3d1b10b5525a0f3c025d1bb08516fab5`

```dockerfile
```

-	Layers:
	-	`sha256:ee054e987c3d05ecb2bf97eb28fea905e4f69b46a536d42bcd72e45498a5bf84`  
		Last Modified: Wed, 02 Jul 2025 15:35:17 GMT  
		Size: 7.4 MB (7421496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:606f0e8ae93d65c70f2948bf448e065256289c94b8f7ca1d21a2aff0ca771df8`  
		Last Modified: Wed, 02 Jul 2025 15:35:18 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json
