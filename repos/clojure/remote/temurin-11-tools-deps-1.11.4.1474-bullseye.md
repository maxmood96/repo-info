## `clojure:temurin-11-tools-deps-1.11.4.1474-bullseye`

```console
$ docker pull clojure@sha256:ea97dfc5520cf0720898591221c133c0fb8c875fee76a605ced8c352d8852d77
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.11.4.1474-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:4ae6cf3ea126c24ab4ae57562656a646a1d6f21c7adf083113d303d11d070306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.7 MB (269729020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc06b6546294b23d99fea4561b4c6cafb9afa9ba6655d4c1f97cc116b56621aa`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:e1bdcceaa316a43ad58ce8cf054a8e89ecf5a0dbae8125eb85e9b26fdb2fca2b in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ba83bbfca9443648a883d1404b33faa0f5e096a99a2b683e3bbaee8912bca845`  
		Last Modified: Wed, 04 Sep 2024 22:34:34 GMT  
		Size: 55.1 MB (55081329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc2f9911486ee6084b498679ca456b43b33b5c94f4c15e37da765b1da85e1c5`  
		Last Modified: Wed, 04 Sep 2024 23:07:46 GMT  
		Size: 145.6 MB (145550068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e623560cb56ab5ebcb710ea7265a522f39d1869416f2c2e8372af56947443505`  
		Last Modified: Wed, 04 Sep 2024 23:07:45 GMT  
		Size: 69.1 MB (69096978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e810ae8591aee1c6b7457a8ec3f4b22c6bcd5fd8a4d98e7ac4bee7b9cbe0264b`  
		Last Modified: Wed, 04 Sep 2024 23:07:42 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.11.4.1474-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:edc1d3caf2b32a73f3f2b247628317e3eca6997251875b992dd354a0452871ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7054209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:699fda7bb69bfb5c5f1fef75abf41db85d456ec26b6ea48131382c0bb4d10cb4`

```dockerfile
```

-	Layers:
	-	`sha256:d056af3089dbf78dac313267b6a81c56d8a55e6092f8bd93e42d54ac605e3fe3`  
		Last Modified: Wed, 04 Sep 2024 23:07:45 GMT  
		Size: 7.0 MB (7040344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5bfd52e259e934c51629cc2e0d4175db8a8bde9644c485da8b1edb4d2ab015b`  
		Last Modified: Wed, 04 Sep 2024 23:07:44 GMT  
		Size: 13.9 KB (13865 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.11.4.1474-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b0b7c24627c3ee07e7ef8e40996915c0d6f6957e500a7c20cf4f5728f63f9e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.2 MB (265178407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17cd82d2b0a85b808a1c27d201b5b72a414f88d0b0e0eefae7a4fd9cf4bfc125`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:4a2aa1b23402547c558d14f98384342f2e98460b659cd211609373f5408e83bc in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:5d8903d6126c38fefcb1196b9998da0798f56cbdf18a91c00d822144c232af6b`  
		Last Modified: Tue, 13 Aug 2024 00:43:03 GMT  
		Size: 53.7 MB (53729921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e8ebc81e83cb3ed4b3fd4fb1931a80994977bb615a00cddc5d409eff357c23`  
		Last Modified: Sat, 17 Aug 2024 06:03:04 GMT  
		Size: 142.4 MB (142354842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef5e746ad41a39b11ce17587a608609ac4d34f7be59fe155ceb5a36e842c4ddf`  
		Last Modified: Sat, 17 Aug 2024 06:08:10 GMT  
		Size: 69.1 MB (69092998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c09026d6aaedcbedf696aa66f65dd98f8870d0de6697ac4de5957ed1679446`  
		Last Modified: Sat, 17 Aug 2024 06:08:08 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.11.4.1474-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:269307aff143d722dedb86ed7882a3f9891a4b6ae47ba4a8f7a06f55d10ae89e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7060467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97acf17ab0e8f52a85d259c6eb30cf6f32acbda0224de4a50505a07fde00a9e9`

```dockerfile
```

-	Layers:
	-	`sha256:18323ed9c910803606c68ebf57b93ead8205a233c8fe5684d3e6f72f4eec2e2a`  
		Last Modified: Fri, 23 Aug 2024 23:55:14 GMT  
		Size: 7.0 MB (7046066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fb46ea45ba8247b92f4752fe4b360dff868b99ca087fb64859d5111b09b3e3e`  
		Last Modified: Fri, 23 Aug 2024 23:55:13 GMT  
		Size: 14.4 KB (14401 bytes)  
		MIME: application/vnd.in-toto+json
