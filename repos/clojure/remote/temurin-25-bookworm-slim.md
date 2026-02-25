## `clojure:temurin-25-bookworm-slim`

```console
$ docker pull clojure@sha256:71ef9fa4d7e37ab58336c892cee16ec08aa2fb7deb9aeaa400649f49c35a2949
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

### `clojure:temurin-25-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:67cf1234986dbdb68b1b9b6e08e141c7281400531e05afc9e89c59f152e240df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.2 MB (190171076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31068a08e63d2b902880a1579f7798f1ea8bb103dd1a5d5aa0b3d28ca566fe69`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:57:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:57:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:57:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:57:24 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 19:57:24 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:57:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 19:57:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 19:57:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 19:57:39 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 19:57:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c680aaf948313775edab478b261700c07edc015c5ae963a95225d1dbcc04c53`  
		Last Modified: Tue, 24 Feb 2026 19:58:01 GMT  
		Size: 92.3 MB (92256275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331c31d53782d34556ab16b292dcc4483d85066546e4ba0dd093954f9ed6523e`  
		Last Modified: Tue, 24 Feb 2026 19:58:00 GMT  
		Size: 69.7 MB (69677481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f090127a6ddec3fdf2ff8c9a32b1aa31d369a468af76906feae802a94bd7222`  
		Last Modified: Tue, 24 Feb 2026 19:57:57 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf87fcc5453fa2b80bc5d3d7841cd10d7efc2905866eb070fe33d7e25d8e2005`  
		Last Modified: Tue, 24 Feb 2026 19:57:57 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6bda6a771908249c0ab4496122343fc49a0f2d11a22c5d303fc438722ab1f18d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5099273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7985bbd5d5c11e294203f0ca2934474d17f95214779f52fcd3169e931da52ec`

```dockerfile
```

-	Layers:
	-	`sha256:b85f4f2a6f45f209accdaffcbd9a42cd828e892a0defe7b7ccbe60babffd8966`  
		Last Modified: Tue, 24 Feb 2026 19:57:58 GMT  
		Size: 5.1 MB (5082748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b978928346a31a8fda7112f2d12beb1929d8d0c381e9ce4241a10ad34f5986a`  
		Last Modified: Tue, 24 Feb 2026 19:57:57 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cbb7e99b68203843cd8ad2724b6c6f75ebe82e17b90da8dcfadbb0a520774094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.1 MB (189078083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:599a0ca2707a8af0f780283c25fe5954133c49dbc6ca2b3efaef2ab18f3706d9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:08:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:08:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:08:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:08:03 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 20:08:03 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:08:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 20:08:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 20:08:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 20:08:18 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 20:08:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d5732d5aa084fcbdd6750b258b128deaf3b98960d035ef5dd79040d0814c83`  
		Last Modified: Tue, 24 Feb 2026 20:08:39 GMT  
		Size: 91.3 MB (91288264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4a0c19c3d97625ea263bafda71cba690192c34385fff1ad526e38e671de5ff`  
		Last Modified: Tue, 24 Feb 2026 20:08:39 GMT  
		Size: 69.7 MB (69672699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1161c46c0e36d69d1d230930a64415d53315b2622ad929cc5b7428dc5e66a20b`  
		Last Modified: Tue, 24 Feb 2026 20:08:36 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aef022da370b8d97dc407779f0068dcefed388e874bfb63ed5e1c0774acd62e`  
		Last Modified: Tue, 24 Feb 2026 20:08:36 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7844cc6c50c106c6811208c5c587d587df80a6a1e359fd769f79163ec21002a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5105197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca4d38c621d6374d488bc98efb1a0c37a04b275f4e93906a00b2cfa666847213`

```dockerfile
```

-	Layers:
	-	`sha256:ac6a0a44ba7ee64aebc515c60763175329b82bd9ad2b35dd15862c6d2a22d22c`  
		Last Modified: Tue, 24 Feb 2026 20:08:36 GMT  
		Size: 5.1 MB (5088530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fd47e0484615410fe2d50d7c0e4c9f62708e44909bad5f3e9f00bc0eda809f0`  
		Last Modified: Tue, 24 Feb 2026 20:08:36 GMT  
		Size: 16.7 KB (16667 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:01c8ec9bb201049e757de33779266a936fb55dfeccceb34001fc17bf620ec973
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.2 MB (199226819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0308097afbd1bfac555449b173b08302f4f867d0a7ca7936011d1e53bbf9e51`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Wed, 25 Feb 2026 02:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 25 Feb 2026 02:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 25 Feb 2026 02:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Feb 2026 02:14:18 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 25 Feb 2026 02:14:19 GMT
WORKDIR /tmp
# Wed, 25 Feb 2026 02:18:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 25 Feb 2026 02:18:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 25 Feb 2026 02:18:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 25 Feb 2026 02:18:41 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 25 Feb 2026 02:18:41 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3def25e912c223ee8b3899e5ca048b2439f856f438ac690293817fbc0291fb36`  
		Last Modified: Tue, 24 Feb 2026 18:41:49 GMT  
		Size: 32.1 MB (32078334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba348ce5bf0fcaa6972e10095c9a06c61641f8395c5fafef888ed9e3e07d216`  
		Last Modified: Wed, 25 Feb 2026 02:15:44 GMT  
		Size: 91.6 MB (91633003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9030998c2aefecdb231ae74d1ecbee720c960e7730fd7883d86d7feb3230575a`  
		Last Modified: Wed, 25 Feb 2026 02:19:18 GMT  
		Size: 75.5 MB (75514440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb00b3d157b73abc6c3e7af516e052cd8e1295e3244a49be23fcdbf6a0deb76`  
		Last Modified: Wed, 25 Feb 2026 02:19:15 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95755e136398af2806395e00161b86ea0f02b41bd4c783e12b95911c8590f41`  
		Last Modified: Wed, 25 Feb 2026 02:19:15 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:406310cd007921d5ebe3edf14175baf03c3c53ada7e2aecb94eb5dae701c7b4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5087815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7c49ba4b94f816037e58fe86fadc70ca6cc359d405e8293d14cc43122737eee`

```dockerfile
```

-	Layers:
	-	`sha256:a700558a655f5e311fb5ff9b601645f759bfee5c3cd834ae6462c0945209844e`  
		Last Modified: Wed, 25 Feb 2026 02:19:15 GMT  
		Size: 5.1 MB (5071230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1bb6328bd76d84a918a967972be73a31e04672b7b86992195214d75db1d8950`  
		Last Modified: Wed, 25 Feb 2026 02:19:15 GMT  
		Size: 16.6 KB (16585 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:4b072e71e3364408da57e4cc06d0a8d70569dae2c3e32062cae6d03fc52c6051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183616592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67880c71842a616368cd410c13519042ae36fe34d08aca913978bfafbfc2ee47`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 23:22:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 23:22:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 23:22:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 23:22:55 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 23:22:55 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 23:25:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 23:25:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 23:25:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 23:25:07 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 23:25:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9bef76beebe598b8ff14a041376f35899cceaeb51a5810f860a721170c7db85e`  
		Last Modified: Tue, 24 Feb 2026 18:41:34 GMT  
		Size: 26.9 MB (26891524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a2c7f155ba43475a58ce53d7548c5de702bcc0cc952b4fe414a2ed67d07e94`  
		Last Modified: Tue, 24 Feb 2026 23:24:09 GMT  
		Size: 88.2 MB (88233846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4844bdba3a0409891bee226bb55ed5541900bb6bac57ef1b0e8a82130a39b1d`  
		Last Modified: Tue, 24 Feb 2026 23:25:43 GMT  
		Size: 68.5 MB (68490178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:010ecee0a42e4f85bef680f38f2c12b0e920e320b85128194b190b15a593e473`  
		Last Modified: Tue, 24 Feb 2026 23:25:42 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884bd627c76a9759a0b55c50a651a8ac45f26d260762af56dc4ad4459ab07ec4`  
		Last Modified: Tue, 24 Feb 2026 23:25:42 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:87c11f263b4337117c03f012861949ccb99b1304e0ae689eeea7c5c015e070e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5075156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f245c25ebf3108e139295f5ed9052894ad9519d337671c5941ec75c0dfd86ac`

```dockerfile
```

-	Layers:
	-	`sha256:feed0721939481d2e5d5f02fb2c27a3f328e8591a4b7e212992dd7c8fc9fae05`  
		Last Modified: Tue, 24 Feb 2026 23:25:42 GMT  
		Size: 5.1 MB (5058631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69436b7d394ba570d09a2abe8f877096f8a2baa2ba707b61f0983289399ab3d3`  
		Last Modified: Tue, 24 Feb 2026 23:25:42 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json
