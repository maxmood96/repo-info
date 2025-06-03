## `clojure:temurin-11-tools-deps-1.12.0.1530-bullseye`

```console
$ docker pull clojure@sha256:b612ea4562603af17e4ed4a361723e04dd3483c40ca7abc9ad6a8a4c37bdf592
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.0.1530-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:fb6a2e94b69db0a03c42fcf293e6763b92101de5fc9ece5f3f60575517ce733c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.8 MB (268785080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5591e6d452d1d73fdb4d93c5197173e6748d6edefd9c65f1fb31838080a794e1`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
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
	-	`sha256:54107f2de180b7b6e9f909d2f1c6c18e10c700a6bd80a035d931768b06bb2905`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 53.8 MB (53750195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da7cf9dd568b115f1f0074b658beb2d4b3b8a42ea1e180b8063d4c5367f6436`  
		Last Modified: Tue, 03 Jun 2025 05:15:55 GMT  
		Size: 145.6 MB (145635604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6f2c82c4304198a36868cbcb3a6a16df39ae1be3a2521546518c8991d70ddb`  
		Last Modified: Tue, 03 Jun 2025 05:15:54 GMT  
		Size: 69.4 MB (69398636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f068c7da7ec1077015582f5789e85c340c43222270eb74a9222f96a6d3f9460e`  
		Last Modified: Tue, 03 Jun 2025 05:15:53 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1530-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:79b1beb3df5159163a47f8c5faa430c0b278eed31940ad09c8298ae9140dd42f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7290579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2f18a895a4bd75f45362543b8598a892bda446723a1e8751e36b64303f4c3cd`

```dockerfile
```

-	Layers:
	-	`sha256:380ce661b045022429dfef4b942c644bd0ea4b1e5858542f8b7abdbcd616b358`  
		Last Modified: Tue, 03 Jun 2025 05:15:53 GMT  
		Size: 7.3 MB (7276327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4b2d16b2cefedb9d20b4dc16cc9d07ee04e9b0aa37d9cf80e9001d0c29a98b7`  
		Last Modified: Tue, 03 Jun 2025 05:15:53 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.0.1530-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:567ce232aec19342c42ca10cd7c373e75839b36fe927dc282cdb43a5e9af4b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.2 MB (264199817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:822e820767568e77d0ff15e4ccf499fab0d0fec6e100af39ccc9e715133d64fb`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
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
	-	`sha256:b2737025fe8da5b868f566cb4e3dc3330028cee06c83db854f56467eca6e09b8`  
		Last Modified: Wed, 21 May 2025 22:28:12 GMT  
		Size: 52.2 MB (52247755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626f26a615782c69600564ba12c678922a75744e8c81f143bbe524275b9c11f7`  
		Last Modified: Thu, 22 May 2025 08:11:15 GMT  
		Size: 142.4 MB (142420720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db981f7fd858c10404457403f2ba3ef9a99e1b4af58c1e7dcf204f5025a71af`  
		Last Modified: Thu, 22 May 2025 08:15:58 GMT  
		Size: 69.5 MB (69530696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e7d687da4f5dbbbc6ce5429a178bab3fc8d9c652f62696e1dded8eb9bee0da`  
		Last Modified: Thu, 22 May 2025 08:15:55 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1530-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:cb14282aec64d24aa2ccab57b445bd67c7b37dfd8922ffa41bbec4433f3fc52f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7294818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:207d6f1af026d85d88ddec63a7ad606d0e2c0e55b689be659247e080674f3211`

```dockerfile
```

-	Layers:
	-	`sha256:0610b455e62034c2bb338913de3c3ec1a31a0bc5e8606edc702dba30697a3823`  
		Last Modified: Thu, 22 May 2025 08:15:56 GMT  
		Size: 7.3 MB (7280448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aea4e0cb91fad888673afb218d60ed3aa2d3854108b3d3d7dc273c1ca98fb614`  
		Last Modified: Thu, 22 May 2025 08:15:55 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json
