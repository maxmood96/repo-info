## `clojure:temurin-17-trixie`

```console
$ docker pull clojure@sha256:e3da18fa4710ecdd99f4545b3c750accf1acd4fff727bc10db1942355b8740dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-17-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:ec4001748a26538c06d233023fcfc356488724295f677bde0db5c25a943f039e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.5 MB (279521945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9475a1a66d1dea7efdf0511183974d7ccb1c0f3ced0cdfdf91e6b79638641cf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:795dbedde24d2c72dafd2b71fe36643552e56859c0e29cdb095ed54b825fbaa2`  
		Last Modified: Tue, 21 Oct 2025 00:20:33 GMT  
		Size: 49.3 MB (49284971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ddeb99909522530610267200a2480b2bb7fe59ce474158e71983014aeaf690`  
		Last Modified: Tue, 21 Oct 2025 10:10:55 GMT  
		Size: 144.7 MB (144693294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96526e5a934edb3539c75da5ff1a3736331393d472d99b5c82c147588f6f27a`  
		Last Modified: Tue, 21 Oct 2025 02:22:53 GMT  
		Size: 85.5 MB (85542636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4baf18d6a685538ecd130f52ac7cef2b4b69a8865b04fc4c00bd9f8170c097`  
		Last Modified: Tue, 21 Oct 2025 02:22:40 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d72975d5043b08ce65adf85bb5ff1a1b07437ac69236c35e5a8f704971effec`  
		Last Modified: Tue, 21 Oct 2025 02:22:41 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6f8bf94fd74b7c966bd6f2fc472bf1ae5f64d003531df221152119a19646235a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2c2e95a9f0a7ca3d0dccd973460634b13c8852c261264d882f775a767234e36`

```dockerfile
```

-	Layers:
	-	`sha256:275f5dcd394a50b49b73920520d2141952d57cd92d3c17c72d63658fb0ce4011`  
		Last Modified: Tue, 21 Oct 2025 09:40:22 GMT  
		Size: 7.5 MB (7466899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e8501778090f5ee3171ffe589ac741b9b031c5ebd6fc4d2ddd1901fddca01b6`  
		Last Modified: Tue, 21 Oct 2025 09:40:23 GMT  
		Size: 15.8 KB (15797 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4d8d9f4c833d8b5d3e964b0dde7354671f6b0873a864258643414e5cfa74d05b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.6 MB (278556028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d9b1ab2ed4a29cb261c49ff45ac546aa9e79e8a9a8b5b21779826b7e31ff2cb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2a101b2fcb53d61db540cb76da094137d4f0291a93fa41357ab70c3debf4d3c3`  
		Last Modified: Tue, 21 Oct 2025 00:22:57 GMT  
		Size: 49.6 MB (49649743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773b1d54405e2ee5849b77d8d82abd6af6d1efbc4bddc05d941d73561e08d1f4`  
		Last Modified: Wed, 22 Oct 2025 09:06:35 GMT  
		Size: 143.5 MB (143542159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f622e6bff705882adea0fee96231c90f758de749ed0dce2aa60803d37faab2`  
		Last Modified: Tue, 21 Oct 2025 02:28:34 GMT  
		Size: 85.4 MB (85363088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f50d91dadad23b6d7d7ea539b02bb66f8d74636867f9a73427366929b2534cba`  
		Last Modified: Tue, 21 Oct 2025 02:28:19 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ea8582fd2bb7ec49d26e7a96236718c81dd3e063554ba0e8cde27208dd1c43`  
		Last Modified: Tue, 21 Oct 2025 02:28:18 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:459bd966079b919eaea231b2b25938befaad524d9cb4c06fbd0e1a9e47b3b811
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7489844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0ca65c0aaa3eea3fe3af20f64858a7d8790a28d731cf09ef3df58eda1f7849f`

```dockerfile
```

-	Layers:
	-	`sha256:2f3e8b2dceac9e009e0d99324fddedc70d92fcf3ad5da3f32e47ed784192c9c6`  
		Last Modified: Tue, 21 Oct 2025 09:40:28 GMT  
		Size: 7.5 MB (7473929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d5e55236cc61f31c6f122c70e00ed926f82b966c1ac24da9079211dbf616d37`  
		Last Modified: Tue, 21 Oct 2025 09:40:29 GMT  
		Size: 15.9 KB (15915 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:2d6830ff1d592a85eba5ce21af7d363c06ceae2914c205c9994bbeab1a4fd997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 MB (288431680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:865c92750e5b70669aca18b8d06754f85a88a2fec05a73cc12a13beedf400471`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:047d1b265d8a7d20ef8b3ccb9f133c3c5f1e4f9c92089889756590b7f20452b5`  
		Last Modified: Tue, 21 Oct 2025 00:26:24 GMT  
		Size: 53.1 MB (53109476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa196e2722380661ec33bed3090b45293b0f65e9e24c95a4205c200872d27ce9`  
		Last Modified: Tue, 21 Oct 2025 15:50:37 GMT  
		Size: 144.4 MB (144372870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1da10d715d7ab1b53b7190d5b526e4ed75b0391bbda656e4ffc4e739ce13a4`  
		Last Modified: Tue, 21 Oct 2025 15:58:26 GMT  
		Size: 90.9 MB (90948292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543cfdaf7c9c3c8931621bbbeb9f63f9a0f0f81cc4dbb2241025e5a2ed098372`  
		Last Modified: Tue, 21 Oct 2025 15:58:16 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02029bd46fdacf86c2a027f3099682190f20a10fcc75352eb80ce4232fa27a0d`  
		Last Modified: Tue, 21 Oct 2025 15:58:16 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f9cd9ad7e2870e05b4bc708cf35bed1de479d843d8358e488e57ffc497832d64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7487163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aafe5285d2e02a3b5a84506df5f886296f5604083d359c617479a331e3e8d4ab`

```dockerfile
```

-	Layers:
	-	`sha256:c412de6ea89c776f8d6fe91aa12e57d244472fd2a9e48635b9fb2d750750c44b`  
		Last Modified: Tue, 21 Oct 2025 18:38:14 GMT  
		Size: 7.5 MB (7471318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:116a3c1325be704255f7a3be1ff16a46aef3262f4d8f33a2adec7db3c56f1cdf`  
		Last Modified: Tue, 21 Oct 2025 18:38:16 GMT  
		Size: 15.8 KB (15845 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:77ab78a9618b94a09e4169577c98125104d3fcd23d1e04dbb9cd86e1249e3c60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.4 MB (273395712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b02b0d10b736c4d9b2e7db508a9f536815464119434fe6f89bec56447f325261`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:913254a25f5e448a50a1e74fa50f037e22f85cfe4d6a3c626f4b7405299b7c1b`  
		Last Modified: Tue, 30 Sep 2025 01:03:38 GMT  
		Size: 47.8 MB (47770009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da301767faf0be7c97a51d690dc02316655fe29df49b482bab04b89ae5a92b0`  
		Last Modified: Thu, 16 Oct 2025 21:34:47 GMT  
		Size: 138.6 MB (138575658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cba5c09ac28f4727f35f1e5a2c38ff6c8a48d3e152a9fdde51787a103cc65b0`  
		Last Modified: Thu, 16 Oct 2025 08:09:51 GMT  
		Size: 87.0 MB (87049001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9879e636406efcfad7103c554b0d0e0a769f48b40893f0cbc7f19dbf04a38d8`  
		Last Modified: Thu, 16 Oct 2025 08:09:37 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1603119e72cd7b55096006f1781edcac19dc66a54e52d7dcf8fb676f83a6babb`  
		Last Modified: Thu, 16 Oct 2025 08:09:37 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:329f2f15823bea64d57700d2e66d47670fa59c460558600fac467227381f9870
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7468738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77eee61fb048ced494868f4a8bfac123c6c3e58efa12d46925a7ad7e5703ac35`

```dockerfile
```

-	Layers:
	-	`sha256:586e4d76d0aa68df31480210268c908bc7c004387ac0f174db1e1e065d2d9270`  
		Last Modified: Thu, 16 Oct 2025 09:37:06 GMT  
		Size: 7.5 MB (7452893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c80954e4cbcc9f956a832195b3f4fccee98bd4d551b3af580a7943c73089c795`  
		Last Modified: Thu, 16 Oct 2025 09:37:07 GMT  
		Size: 15.8 KB (15845 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:28c3459adce3a58806988df45949aa778e4654decc71c219b3d0142082b6c84f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270582788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d86751c44222bb70b86b295416a58fa830df065c464e44f383e2b4f74ea6202`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:be7c8533c3f8dfcf5ab5c0fd76b47a568dc971c853834a20808defd1e88a5ffe`  
		Last Modified: Tue, 21 Oct 2025 00:27:58 GMT  
		Size: 49.4 MB (49351699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2cb6faf67122655d0273930a2abef9e556dd9ecc56144907d685ba5dfb5b8ea`  
		Last Modified: Tue, 21 Oct 2025 22:08:59 GMT  
		Size: 134.7 MB (134723657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b59ffc2dfd081457fd0e602992ea6cce749af22c16c17f3a601ab605e52e7f2`  
		Last Modified: Tue, 21 Oct 2025 22:21:22 GMT  
		Size: 86.5 MB (86506390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aec91f07f82feb2e2cf2f3f7d7ab6c2776f6126db2b94aad856bf49419753dc`  
		Last Modified: Tue, 21 Oct 2025 22:21:15 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd875e46c344f80259add62125b0ffc8c98c5bf6fa2e878654d0208c3544112`  
		Last Modified: Tue, 21 Oct 2025 22:21:15 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9ae387c68f6fad7a73000986b739bdd153508398b778082ed8b49a4d97437746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7478618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19cae2925ab881e90d1e642333aacb9f1a996972d001d34222a521a6c7da399f`

```dockerfile
```

-	Layers:
	-	`sha256:6920d36ca6e6a0d141faf844ca457afb31efb6e104e0156fdabb83fb12e4b2a3`  
		Last Modified: Wed, 22 Oct 2025 00:38:02 GMT  
		Size: 7.5 MB (7462821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:677d9d3b554855be4b6d4e19b108f5880dcd6efaad12183bf79c450636ccb568`  
		Last Modified: Wed, 22 Oct 2025 00:38:03 GMT  
		Size: 15.8 KB (15797 bytes)  
		MIME: application/vnd.in-toto+json
