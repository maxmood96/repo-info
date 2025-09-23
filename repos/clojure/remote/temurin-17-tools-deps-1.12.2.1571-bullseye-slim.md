## `clojure:temurin-17-tools-deps-1.12.2.1571-bullseye-slim`

```console
$ docker pull clojure@sha256:cdc9c43019364c378dccb2d159dc957d0e993cfcb59c97556f56ca5dc2c4e16d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.2.1571-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ad9cbfb15f55894342e3dda7a0672fead36eb74a10f8701d0c0683cdea22efd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.1 MB (234104285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aebfc39a8b50c9b1df84edd9e6306fb68f196b716d673394de3a23509d42e01d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:456a3213e1b1f193dc759cd05f6f8422428b8c4bd45ef40fbf41ba43bdce8570`  
		Last Modified: Mon, 08 Sep 2025 21:12:48 GMT  
		Size: 30.3 MB (30256068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db36db229cef31c3d84fbfa3aab6afabc50462fa08d3ab85c18e4bbdefcaac22`  
		Last Modified: Tue, 23 Sep 2025 01:45:36 GMT  
		Size: 144.7 MB (144693604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa82edb6a083e670b4b3034f834e05a71c1ee37f5ac8572e7b087c6b5b13f1a3`  
		Last Modified: Mon, 22 Sep 2025 23:46:05 GMT  
		Size: 59.2 MB (59153571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e782074f01eb644c01665d7ef2b8903410df73056645df8bb2da060021538aa8`  
		Last Modified: Mon, 22 Sep 2025 23:46:00 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a45472f46a444db916b47761a5742c948bf712cd8776c82d2578f266f8d68774`  
		Last Modified: Mon, 22 Sep 2025 23:46:00 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.2.1571-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d05ce4300de3efbf926f7e7b5996123a475c2532d23437d7dc56cd2efd2ec148
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5323946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e4509e4ba183f960d607b8e2aae393e5ccb3c4368fc4a537341732cd072b5a9`

```dockerfile
```

-	Layers:
	-	`sha256:e7ad11544afca7e59419dc3bfb7942e37fc3eefa9a248aa8d2579c21f9c030c1`  
		Last Modified: Tue, 23 Sep 2025 00:38:16 GMT  
		Size: 5.3 MB (5308067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d2f45a839593e3a436ef01682a72bb537fc073f2bc4a413095c3caff2c1703b`  
		Last Modified: Tue, 23 Sep 2025 00:38:17 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.2.1571-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c9b43aa08d804b1c365f9d0d866ffb755a81aaf1e99b871c2756e86f20dfd88b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231580913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6712ec550f452944b8ab8629b828cb587ee5edc338d6de394766ae3a64bc8ee7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8568e9af3ab25a29d98aac9a07896467a19253e72e5be0cf09cd3982ac4444d0`  
		Last Modified: Mon, 08 Sep 2025 21:15:52 GMT  
		Size: 28.8 MB (28750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8e237819fecb6ec4bb1ce0a7c42bfe64ffb4267b22f1da6f852651acffb30f`  
		Last Modified: Tue, 23 Sep 2025 20:35:08 GMT  
		Size: 143.5 MB (143542130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df036827c0d3a29b8457aaba51c91276ba8dd1822302f608ff881748346e06c8`  
		Last Modified: Tue, 23 Sep 2025 20:35:01 GMT  
		Size: 59.3 MB (59287282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834811372b7d4c38a351bef2b67bd2f9c9712c039ab324f40123a7991d2f916a`  
		Last Modified: Mon, 22 Sep 2025 23:07:11 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb72cf46716e837dd72a9970f884b741556579160edba30be953c530f9f350c`  
		Last Modified: Mon, 22 Sep 2025 23:07:12 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.2.1571-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:091939e89d2e99c0c45ef91b6afc707aaf4afd7c22cfaecacf49d4b76bce9981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5329796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6148db1f41878f2153763db340ba4b77adc4d9bfbb71b56056b9f0049c3907bf`

```dockerfile
```

-	Layers:
	-	`sha256:0c406e7f454bfe70c3bb8f507359aee4b04db31ebee776d0a3133de1353e3c99`  
		Last Modified: Tue, 23 Sep 2025 00:38:22 GMT  
		Size: 5.3 MB (5313799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21d0b5f69e4bf5fa704b63165807b72044e76432aca041f358cef357049e6e0c`  
		Last Modified: Tue, 23 Sep 2025 00:38:23 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json
