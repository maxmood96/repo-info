## `clojure:temurin-11-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:806acaabf7de9bb27514452b72f447880f5f426761468a669cd46ff7e2bdb729
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:671c15f6b8df2e17fe50e1d2039598a17f08991963dc75d6f00a6fa02a4ce43f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.8 MB (268800822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb08826b834bfaa848ba97e2c69b8811c186d7ec3bb85b140a149ee6f1bf59fe`
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
	-	`sha256:1fafc410dbfc5c280bb256fe5797af0052ee6ac8ab95422ed486e79d7bb0608e`  
		Last Modified: Tue, 01 Jul 2025 02:38:59 GMT  
		Size: 145.6 MB (145635640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce673f94f27350fc77add0c022568d21858bbe135f184cf0fff99fe7a268cb74`  
		Last Modified: Tue, 01 Jul 2025 02:39:17 GMT  
		Size: 69.4 MB (69409717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd365c7406c903d388e11e2834238b5d95f943e8ec611463bd9db87f0238c9bc`  
		Last Modified: Tue, 01 Jul 2025 02:39:04 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:d41e278a68feb0cd65d5bfbaa748e097fa927862f70de172df08a36092e78f9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7430031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f8a39be7e885181830439d97c58eccd2276f50fc2e28a34510d7f920cef0e0d`

```dockerfile
```

-	Layers:
	-	`sha256:7028d69a42fc6a143ea383b682ac0cc23fc9f8ea60d349fd0d1d817daa2e2e19`  
		Last Modified: Tue, 01 Jul 2025 06:35:24 GMT  
		Size: 7.4 MB (7415779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9d24d5501c6700731d4d4bf9f6b7c679af78be33564abcb15bbf6eaa655de14`  
		Last Modified: Tue, 01 Jul 2025 06:35:25 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ea9703261b2a5383477d075bbe8ff1d64304f3d412046bb7c29a89960a6e6512
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.2 MB (264211036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b4b2cfd17ae452c3279b0d623d7f31ee640ee7c59e7e6a33efb84eca25a8b93`
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
	-	`sha256:d0b068decccd3f64ab597744c3957bac88f2e12d807a02f894920187eca517cc`  
		Last Modified: Tue, 01 Jul 2025 12:07:11 GMT  
		Size: 142.4 MB (142420643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ae19b8e2f58d1de180c89df0090edc9e124ddc58ea140820eacd6893122eac`  
		Last Modified: Tue, 01 Jul 2025 12:14:47 GMT  
		Size: 69.5 MB (69537498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76dca4b2bb2c1d564d6e19d51366d2d10c90e2ed3277e74618ad049951aed33e`  
		Last Modified: Tue, 01 Jul 2025 12:14:43 GMT  
		Size: 609.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:6df7b6ca156c6f7967a85e21a3440022966c13236db2b347367351d603eb0358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7435866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5810046c5111bcb52c57fa25cdfeae59455925c1a20f9521d978dcb4c2b28987`

```dockerfile
```

-	Layers:
	-	`sha256:900298bd420e6f1b0d35546732078a2659a10228869115dd9a38ea736d05707b`  
		Last Modified: Tue, 01 Jul 2025 15:35:15 GMT  
		Size: 7.4 MB (7421496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a792f07f74eeebf56fb752c80f1f898ed3e7c3d63aee4863b63c778a2992787f`  
		Last Modified: Tue, 01 Jul 2025 15:35:16 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json
