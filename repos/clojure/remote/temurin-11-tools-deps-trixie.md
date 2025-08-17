## `clojure:temurin-11-tools-deps-trixie`

```console
$ docker pull clojure@sha256:8e08e05b3c4586ff0561c23155fd2035639c6479a68bf583a357539b0aaad111
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:884e22065c0bd18937ca50686aedf64595e3c164a86db376dae4f9247be3d593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.3 MB (280322858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:597f0bde014f0fc1f4e7521f33de273e3370d2f02e1bb45ebf1d6997eb3ef925`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
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
	-	`sha256:80b7316254b3093eb3c7ac44bb6c34bde013f27947c1ed8d8afe456b957ebfdb`  
		Last Modified: Tue, 12 Aug 2025 20:45:14 GMT  
		Size: 49.3 MB (49278280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce27b554d2d53ffdafbaf72f22cc3f7023f17836adcc9a6723212e8fa95290bc`  
		Last Modified: Wed, 13 Aug 2025 21:52:17 GMT  
		Size: 145.7 MB (145658173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f026c088799b73afe0e0c8a72d876f7745eae5566d5d72fd1fce8ae1df9f3c95`  
		Last Modified: Tue, 12 Aug 2025 21:36:51 GMT  
		Size: 85.4 MB (85385762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0bf029877dcdd60a049b23b84198a49f981d565bb76ba2c136f0df71d9bd18`  
		Last Modified: Tue, 12 Aug 2025 21:36:36 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:bfcd13ddbd159cfbdce3579ebbf72fa5e90fa8766836eca21bf9e67448a01412
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7496560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27d6035655a084c51586e5b0e7c2061729353c722bea6b3b09d90c3281e3fa4e`

```dockerfile
```

-	Layers:
	-	`sha256:2128cd8420485dd096c2a4f85f437c112a20408edafca4637472108a52fd4b98`  
		Last Modified: Wed, 13 Aug 2025 00:36:22 GMT  
		Size: 7.5 MB (7482333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12e2afd1529a1aa3ff3b87da62ab9863ba1ed8863b19863b4cd2e7da14f85ee3`  
		Last Modified: Wed, 13 Aug 2025 00:36:23 GMT  
		Size: 14.2 KB (14227 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a48517e7f42ae63aeff799e159b6e1036ffaa469ed56db6435d6b45c7b50a160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.3 MB (277313544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7baa67c5bb1f182b16d60923d2c161bf463642d2058e42a28276b18d03c9c97e`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
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
	-	`sha256:d1e40442030765a3ac5d135c39154d052eba20953ea0e5d35a066f7722cdd93d`  
		Last Modified: Tue, 12 Aug 2025 22:12:36 GMT  
		Size: 49.6 MB (49641603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784b185fa6d2d9738346853b610ad4ced4884b6eef61ad14c28c89e7ec1d1227`  
		Last Modified: Sun, 17 Aug 2025 04:50:18 GMT  
		Size: 142.5 MB (142460541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b13e7f445de9bd5c3cfdf330188053eff54bda1537eb64043076f9884d9494`  
		Last Modified: Wed, 13 Aug 2025 14:19:53 GMT  
		Size: 85.2 MB (85210754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684d7d4167a3976e2663da7cf543cc733f73b93b7d3ea6f12d170c9ca4a4e6ae`  
		Last Modified: Wed, 13 Aug 2025 14:19:35 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b0c8b48a786c853ee518f32ef4f7620577bdcfda7f4e5bb9aa6c1707f63a6d92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7504327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d0ad303a8734421d2fc4f281f4c14b4d496c141b8cd8b9936920c5fb7721c4`

```dockerfile
```

-	Layers:
	-	`sha256:43c521cd272ac8d4695efeddb549fd747db199f718e254e936d6610457c0b83c`  
		Last Modified: Wed, 13 Aug 2025 15:36:32 GMT  
		Size: 7.5 MB (7489981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fb441279c3175ac8350153a5812f361c0455e75399ff333fa995a0df8bf1c4e`  
		Last Modified: Wed, 13 Aug 2025 15:36:33 GMT  
		Size: 14.3 KB (14346 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:45a3fd89f36e3684f1c2d6b0a20b34429027456f03b8de1c946c3b3283488c88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.8 MB (276752247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9c7cfdde70c48a5402987e2f6047f29873ee39548551a23692769cee83c59eb`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
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
	-	`sha256:befe77620590f63939f5bcadadc9f45832981822c9c901f057eb4e86f733c29a`  
		Last Modified: Wed, 13 Aug 2025 00:32:04 GMT  
		Size: 53.1 MB (53103384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a0f3ccc9d08f604a4e4588ee702bba4449f64fd505b563f80df5ad4979b526b`  
		Last Modified: Wed, 13 Aug 2025 19:35:39 GMT  
		Size: 132.9 MB (132853298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736bf6edcd56aa650defb243921730d0c3ffae7b8d1056a47efbea8e85f3cda7`  
		Last Modified: Wed, 13 Aug 2025 19:42:39 GMT  
		Size: 90.8 MB (90794919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63f97ebf895a00e550ef1639e8ee8e3bd547bc50ae1339b417b961626d1eb61`  
		Last Modified: Wed, 13 Aug 2025 19:49:15 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:34a1e1ca05f952e404738e2645881beecbe152bce76e5e61e3c8986002f419db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7500413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f37416074901307dceaa7042856e4016f2d4f49bf858c2d13dfae24aaa8ee97`

```dockerfile
```

-	Layers:
	-	`sha256:932461ec8782032a6e3de04550d99fdd56ffd6296d8889b7285d0a2403a1d87c`  
		Last Modified: Wed, 13 Aug 2025 21:36:06 GMT  
		Size: 7.5 MB (7486137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fc14d335632753719efa2c46762172036965a70eaf6bc4d8486fecf251b82e1`  
		Last Modified: Wed, 13 Aug 2025 21:36:07 GMT  
		Size: 14.3 KB (14276 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:d6cffeff436cf75c7baf8adcb4e3551322c6acc8f0362953fc929100f1798a22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.3 MB (261321629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82ac81e2d96d6e3a923d9103481df638a23a441b70ee03742778bbd39bf5fdff`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
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
	-	`sha256:c3b791adea90b39bc59919a9959b7f44f65aa3364a03dd0271a5ff658488877f`  
		Last Modified: Tue, 12 Aug 2025 20:59:03 GMT  
		Size: 49.3 MB (49345161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2661e720933e28bd080f383797ada03de8d9857706acc0b35f53e54b00b23e`  
		Last Modified: Wed, 13 Aug 2025 09:17:51 GMT  
		Size: 125.6 MB (125622113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94968b2c52a04d59ac400eeb344340bab355fe6b2930977bdd0bd3fb3e3b63e4`  
		Last Modified: Wed, 13 Aug 2025 09:17:59 GMT  
		Size: 86.4 MB (86353710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e587a3e2ff2a5b5f2b6199316c7c061ad64b0d66e4f513cf0ae797848106a51`  
		Last Modified: Wed, 13 Aug 2025 07:09:51 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8c0268c6c6f00f25c4a67cdef4507b21f340c9d3a32248744b84a8008311ab38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7492487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1c00617748ecf8fff47f6c901fe181360614b464f11d276ab6acf016f8f7289`

```dockerfile
```

-	Layers:
	-	`sha256:f052b38d88dc7b672f55a590e9aca3e2c500ed1b0d4817e595572a61fd7683b8`  
		Last Modified: Wed, 13 Aug 2025 09:35:48 GMT  
		Size: 7.5 MB (7478259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d0a9fdb612e741a21e56f6845f3ff92609f225fe3e8ee067c0d9e224940cd54`  
		Last Modified: Wed, 13 Aug 2025 09:35:49 GMT  
		Size: 14.2 KB (14228 bytes)  
		MIME: application/vnd.in-toto+json
