## `clojure:temurin-11-bullseye`

```console
$ docker pull clojure@sha256:dd872c02620945c929d4312e5fd2e3428856d1bebe26f9d41ed1feb079b5eb23
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:f7bca990cee77441b556b7a975af2b946bb7c8ab114d878e44361f88800acdea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.8 MB (268796301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e04fa0f90f8dffedc8f0c4220df082a4a1247deb4c15b9f656c445f5f317ae20`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
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
	-	`sha256:54107f2de180b7b6e9f909d2f1c6c18e10c700a6bd80a035d931768b06bb2905`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 53.8 MB (53750195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9036b924b63e31b1873ddf51942c0b6aa36f27dfd8b65a8e9fd790ace943beb`  
		Last Modified: Mon, 09 Jun 2025 17:17:51 GMT  
		Size: 145.6 MB (145635655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eff1ed934e79ccde9b73862aa142a8f8011dbf36117c9ba79b5d8488a33f5979`  
		Last Modified: Mon, 09 Jun 2025 17:17:50 GMT  
		Size: 69.4 MB (69409808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef886f460d029c3adf17be854d04af83ea52e8997535ce9d8dc52ce1096a5ac`  
		Last Modified: Mon, 09 Jun 2025 17:17:49 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:4f5452b1df8d989353b54dd4e88b69052be5218c3b720febad47f39f94ad2999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7431655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:598affc6d016edb8689cb408050daf800e74731e641e5ca5a407108aacc85e20`

```dockerfile
```

-	Layers:
	-	`sha256:f51c2c17f6258b003b9a9ffcea7d7f8b08e6554161ace335dd221da6d6baafd3`  
		Last Modified: Mon, 09 Jun 2025 18:35:07 GMT  
		Size: 7.4 MB (7417403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9857313258f31a0d713a0b56d7de058d31b9fe9acd6fadbd5aec583a5d8f3b10`  
		Last Modified: Mon, 09 Jun 2025 18:35:08 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:66de2c37c7f1504d50140bf98df630afb31d695e7bdc211770fb237260202685
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.2 MB (264206808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f746159b783a4540e75736ab8cdc3abcbfdadf5f6e97e8ee73065ef79a6aa29b`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
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
	-	`sha256:b2737025fe8da5b868f566cb4e3dc3330028cee06c83db854f56467eca6e09b8`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 52.2 MB (52247755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdd289c7253c53f059da906341840e1077ab6a119d05f64b8c6dff33cf8bed3`  
		Last Modified: Fri, 06 Jun 2025 13:17:09 GMT  
		Size: 142.4 MB (142420650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba5298936c8de24a82c35882f6ae90c6c56ed5607db291c1a44af09229c402b`  
		Last Modified: Mon, 09 Jun 2025 17:40:46 GMT  
		Size: 69.5 MB (69537761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e404cabe89cfa2c6d3ec0c2cad02389aacca962a5c675763a078bb1edea1a902`  
		Last Modified: Mon, 09 Jun 2025 17:40:39 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:34cb85338f3aea546df066a68aceaa1d8231ace3de0191136379dc81757c4548
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7437490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a5f05812f73fbb8e5902fa18a2ba048c2d3b976cac92ebadb848090175cff40`

```dockerfile
```

-	Layers:
	-	`sha256:ea15c8d51e1dd87bfa67c0c9e83b0442db6f6d915b0827465cc3494d684a8a56`  
		Last Modified: Mon, 09 Jun 2025 18:35:14 GMT  
		Size: 7.4 MB (7423120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba0f18ffef02f5c2be8db5c046b1114487d3f51e3468e2fe736241fd4d51cfda`  
		Last Modified: Mon, 09 Jun 2025 18:35:15 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json
