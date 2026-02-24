## `clojure:temurin-25-bookworm`

```console
$ docker pull clojure@sha256:96a63517a5fa77511563293fca21b62cf7f652f01aaef5ec65c1b811ff9bcd40
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

### `clojure:temurin-25-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:1b99c20d75fac5f979bd640f254c668ef9c4f21e726087aad131080e554dd8f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221896621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fdfacafe769e3afef20d374ae20f1da01cf89ef5cef8a91ec0a6238efd82126`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:57:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:57:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:57:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:57:10 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 19:57:10 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:57:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 19:57:27 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 19:57:27 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 19:57:27 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 19:57:27 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2edc6fc8698289953a24180c95b172dc14969bcd79196a912bf1616786e1bc19`  
		Last Modified: Tue, 24 Feb 2026 19:57:49 GMT  
		Size: 92.3 MB (92256301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a580010313838a210477b6489c926230254a4f92e892ffbf0a3f7293e072cf6`  
		Last Modified: Tue, 24 Feb 2026 19:57:48 GMT  
		Size: 81.2 MB (81150504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3fcdc6bd5736bafd15ca38e8d8a0c1367a687bf5b814234f6ccda57deb6458`  
		Last Modified: Tue, 24 Feb 2026 19:57:45 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d20bee70fe51603ac8e8e0661ce579d037e342aded20c47c4b954fb2a95c01`  
		Last Modified: Tue, 24 Feb 2026 19:57:45 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c3478626e710b296f10db487f53c90d66c45ab681a373751070b3c8c5d65af5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7363958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79523775196edda900acbd88093d0253441310249a65beb75ab817887798d793`

```dockerfile
```

-	Layers:
	-	`sha256:05a2a44229dc93084635bfff20cda93d8352eaed944b93ee6c2591642f000c7d`  
		Last Modified: Tue, 24 Feb 2026 19:57:45 GMT  
		Size: 7.3 MB (7346187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52d8a7b49f8241a828c13259fc43bbef8bcebfb5b2a52359ff82fd31d63e7c46`  
		Last Modified: Tue, 24 Feb 2026 19:57:45 GMT  
		Size: 17.8 KB (17771 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bac0bfc00c1bd24b76fc263e1a0c44d05aafb1697c9a9740fdba381c862abadf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220800872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de02eab498ca60e22f3364f92cd02c863073166a134ad21eb546e94dd815268`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:02:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:02:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:02:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:02:24 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 20:02:24 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:07:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 20:07:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 20:07:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 20:07:57 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 20:07:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c81c80c7b69e4e786d3000ed02b7684f04659ca1951d1bf428f7793956815d`  
		Last Modified: Tue, 24 Feb 2026 20:03:20 GMT  
		Size: 91.3 MB (91288274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865ebc8347ab5ada1ef115cc1b446a621fb6fe452257f6ff8d476665c24548e1`  
		Last Modified: Tue, 24 Feb 2026 20:08:16 GMT  
		Size: 81.1 MB (81138348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b1ddb319225690109278b5a833b2c22033762fe758f73d6f06360fd97d3bc0`  
		Last Modified: Tue, 24 Feb 2026 20:08:14 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea60044ec5f10e8a73ae1b734e9d20a5d3b7e67fb9e94a004debbae618b97a4d`  
		Last Modified: Tue, 24 Feb 2026 20:08:14 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b877219d40f437192e101b2a8ee11e7c4430d30e591798b1668222e4e07295a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7369181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3398482bf897a9fe5dfb7d61f500d692213a85e46707c120ab4f92a3d8d489b`

```dockerfile
```

-	Layers:
	-	`sha256:c33b14727e36399c80b1afba78fd7e1032202cf6fe9b4813acc1a9899ebfe0b5`  
		Last Modified: Tue, 24 Feb 2026 20:08:14 GMT  
		Size: 7.4 MB (7352019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:498aa50cf83b65192ee7945cc95b4d266e1b5aa10f2c6e369b689b3297e59d67`  
		Last Modified: Tue, 24 Feb 2026 20:08:14 GMT  
		Size: 17.2 KB (17162 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:d6ae605ebfa8ff4fed2d498549cb066429940de7d04761f878294ad6377e7666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230948403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:013035f48441564da0716e6492aaf8eba05226dd57480f94a56ce3f641f6809f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Thu, 05 Feb 2026 23:54:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:54:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:54:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:54:17 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:54:18 GMT
WORKDIR /tmp
# Fri, 06 Feb 2026 00:51:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Feb 2026 00:51:15 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Feb 2026 00:51:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Feb 2026 00:51:16 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Feb 2026 00:51:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5e189aacb842725e8d1d9877c9ab9af09e14901412b6665e179393112b5bca51`  
		Last Modified: Tue, 03 Feb 2026 01:12:57 GMT  
		Size: 52.3 MB (52327289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413bd0b8c6c326da16c676c4dc2f9ba6260e745418e4f97b3a2d3fb7fa2bf0a6`  
		Last Modified: Thu, 05 Feb 2026 23:57:00 GMT  
		Size: 91.6 MB (91632873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff49bdb92c29d1aa0a5728614463126c1cb70700342bdd4563bf11bcb84f9c5`  
		Last Modified: Fri, 06 Feb 2026 00:52:01 GMT  
		Size: 87.0 MB (86987198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7846677a8fe0a48bbcf1c1e4fdeb070ff23256f19e07d916a49d6ce8dbd9402`  
		Last Modified: Fri, 06 Feb 2026 00:51:58 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:071f8bfc37cc85641a427ac9f96190881bc3f500b3a164f6dda5b316b54df8e1`  
		Last Modified: Fri, 06 Feb 2026 00:51:58 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:66d651449302ca7e6546187bf2bf1edc83d83d991230b8c4146195df6ead2c1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7352606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6f0ed9164abe7d142a39132a6b06630c6ce4caf786ba58895f29c00284a10a1`

```dockerfile
```

-	Layers:
	-	`sha256:dd595615a846cb5160d99a3436c3b535a4f54e73ee25d800989941ce73a4a513`  
		Last Modified: Wed, 18 Feb 2026 00:05:38 GMT  
		Size: 7.3 MB (7334751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:372637b1f00263d522dd60f039aa47b548c7d138e905e41093fd6fdbb325aab6`  
		Last Modified: Wed, 18 Feb 2026 00:05:38 GMT  
		Size: 17.9 KB (17855 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:88c92c54be70a46a4acb137dddd277d53865a0b5b2a0f1a5bf80fafdef58a6b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.3 MB (215336889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5251ae2a9ae5cc3aeba6c858127cb04e823c16f3053bc012c41cac367a33674b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 22:16:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 22:16:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 22:16:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 22:16:01 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 22:16:02 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 22:18:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 22:18:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 22:18:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 22:18:33 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 22:18:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4c4c4621da5085342b3b0d8d8ef57e5e44004eedf5818268af30c41a02cb6cf2`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 47.1 MB (47138343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfba6fd0c0d82ea9631bef0d5f1a77cdb1ed5e84260880b88825e90f3037036e`  
		Last Modified: Tue, 17 Feb 2026 22:17:20 GMT  
		Size: 88.2 MB (88233833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfbc43a3c9ee33d9356cf1da6742e2ef435798f096b157c04bcb8817208f7403`  
		Last Modified: Tue, 17 Feb 2026 22:19:11 GMT  
		Size: 80.0 MB (79963673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe99df8668f427140a412788e2d3de2daeb5865f760932b0a29ada3d39fa0271`  
		Last Modified: Tue, 17 Feb 2026 22:19:08 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8601577e897e42933a2997338df395dee8210868efc3efa89e5fdc7047cd538c`  
		Last Modified: Tue, 17 Feb 2026 22:19:08 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:1bff20358a8f7fd8f6b043bbb5bc6418b6045d6d00a6cd08c4b00ddee169e34c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7339838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6742b191bb98931a989d7e4e2a59fada7bb32dca264356a927adf239fddbb41f`

```dockerfile
```

-	Layers:
	-	`sha256:dbfb8a3633211be94d5f5af2bb32df00c72b9f3491f0342909257fa53ff45528`  
		Last Modified: Tue, 17 Feb 2026 22:19:09 GMT  
		Size: 7.3 MB (7322068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13d1d226a4735dfd3956f317295c8074ef61d967ed32d0f282dcc8264ae14575`  
		Last Modified: Tue, 17 Feb 2026 22:19:09 GMT  
		Size: 17.8 KB (17770 bytes)  
		MIME: application/vnd.in-toto+json
