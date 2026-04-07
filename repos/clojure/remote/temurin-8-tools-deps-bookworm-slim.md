## `clojure:temurin-8-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:d8e0a2c962d0ff4a3805e9693141db2eb78ce514ebe5088e3e25772e7dd14fec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e3827b24e73eaf9a9482de731fba0f69418fb307d80aa1b10ef21f36fc3319d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.1 MB (153108611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55a61622f85a4bd5083bda1ad076022b2162f47d3b7a9dfc028f45a1227a5677`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:12:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:12:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:12:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:12:46 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:12:46 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:13:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:13:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:13:00 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f453da7b3daebeed59cd2f4ba5c8a60d6ed3a84fb931a7acdfee939bfecaa8cf`  
		Last Modified: Tue, 07 Apr 2026 03:13:15 GMT  
		Size: 55.2 MB (55170190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fca18bbad692fe2ef9d1ebce1dd5a22230ca3dfc899ab153fa59fb09d48df32`  
		Last Modified: Tue, 07 Apr 2026 03:13:16 GMT  
		Size: 69.7 MB (69701442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a32ac74a1ab86a16556f777a4d752e21e752811c464c730c312d976d04cb03`  
		Last Modified: Tue, 07 Apr 2026 03:13:13 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8405995c5b3cce56d90694e4afe593d0492f45d4c2a74aa3e65d89489d40fe4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5251400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:189fd462ed09b309ee505c429930b5c706edb6480aa82132878871260ba51999`

```dockerfile
```

-	Layers:
	-	`sha256:9fbfd28e5832a26697acf04f91cf05fd4ef48e2ca50d7c656ae3ad595d627875`  
		Last Modified: Tue, 07 Apr 2026 03:13:13 GMT  
		Size: 5.2 MB (5237154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08b71804898ab47945a2e91da562961504e2343fbe39ff79dcb7c0ea95d74b59`  
		Last Modified: Tue, 07 Apr 2026 03:13:13 GMT  
		Size: 14.2 KB (14246 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f1c314a4ddf7c3b1749c70f10fd0d2e8e8455a15044a26c7c77bbc5d8a6f7673
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.1 MB (152057405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a8f72eb56ddd37563c76d42c45da0e70b7af2f0d4b69b8a4d250eda4b0881ea`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:23:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:23:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:23:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:23:30 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:23:30 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:23:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:23:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:23:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d6e595111a1b4e74740bc6a5a1d2cc6adbf096152fe0b40a97c5dbe2ac6e441`  
		Last Modified: Tue, 07 Apr 2026 03:24:03 GMT  
		Size: 54.3 MB (54251612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a0c2007f1673f4260893aace248c06cc90bf7ffba42cbd8ae28fd2a64ca847a`  
		Last Modified: Tue, 07 Apr 2026 03:24:04 GMT  
		Size: 69.7 MB (69688981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee628e83ae2c471dd3f9184d7682fe2b0cf333584907bd4aef4e7f0e78243a82`  
		Last Modified: Tue, 07 Apr 2026 03:24:01 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bdd0de2047c7149a1cc8b09f9d3864ca3822d5b361100e885a227b957ba666f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5257981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dde0894f58b14203caa25cfcfead9bfc0fb17f9e486ce084b395d0113054827`

```dockerfile
```

-	Layers:
	-	`sha256:149059f0f6637ddf2c88f77428addd7236d09c3831905680a17985cdb3ebacc3`  
		Last Modified: Tue, 07 Apr 2026 03:24:01 GMT  
		Size: 5.2 MB (5243615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8f40122de3a8e9481c9bdd1fde3264c0ebf67dcd2592adc8a8b232687e77364`  
		Last Modified: Tue, 07 Apr 2026 03:24:01 GMT  
		Size: 14.4 KB (14366 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:16253d6f0a6e33f42e58b99399ac893bce86b26a17a57871ffea8f9cc33419b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.3 MB (160262880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0f3f26d7056d7a0e97d9a2daec6185627138ad8317f6498fd8ed6fd82f6b426`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 18:06:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:06:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:06:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:06:19 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 18:06:19 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 18:11:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 18:11:03 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 18:11:03 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7a0392d98c02d4219c67a8e3d3837c1ac5d4af6836b9264bdd6c427cc7a24f76`  
		Last Modified: Mon, 16 Mar 2026 21:51:26 GMT  
		Size: 32.1 MB (32078368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d87cd97df95540bc764bd675651a228c43a8bd513ce7d2048e612519e294f6d`  
		Last Modified: Tue, 17 Mar 2026 18:07:15 GMT  
		Size: 52.7 MB (52650377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834f97609ec0860c0497921916bc81aa52f30a37820a38cb43b09fa60a2f401e`  
		Last Modified: Tue, 17 Mar 2026 18:11:38 GMT  
		Size: 75.5 MB (75533490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5cdb70a8cf08091d585cf88a8109f83a2667943f4a027bb7236ef83df855fd`  
		Last Modified: Tue, 17 Mar 2026 18:11:35 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:69e68945e7b262a4b174a028d6c42869cd988164b6d7659a3572ab8b30486fb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5257203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f014e0808b3f94cb6d882c88c3c50fd3bb65dece403b80f2efe46b2ee753d056`

```dockerfile
```

-	Layers:
	-	`sha256:189f6890a72d816ef56f42a60d56f3c43597aeecd0e20ca6d1e2a23d0c6c2dd3`  
		Last Modified: Tue, 17 Mar 2026 18:11:35 GMT  
		Size: 5.2 MB (5242907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aada4c94cefe8fc4de3cc4bfce410751898d90b3381bdec12db7ec39f6edef86`  
		Last Modified: Tue, 17 Mar 2026 18:11:35 GMT  
		Size: 14.3 KB (14296 bytes)  
		MIME: application/vnd.in-toto+json
