## `clojure:temurin-21-trixie`

```console
$ docker pull clojure@sha256:b15c6bfd64746caf736e9060ce28f4f6cbf1693820b4ab46bf6f0de916eab62e
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

### `clojure:temurin-21-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:8603ccf129c553cf7ef437fc2146479f874940526bc32aa1833255e2119aad69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292690620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:628ea0f105d5e8b73bdd5ade6cdec75cb21980c80b055d4c10f66676e9efd82a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:56:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:56:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:56:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:56:27 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 19:56:27 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:56:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 19:56:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 19:56:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 19:56:44 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 19:56:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:866771c43bf5eb77362eeeb163c0c825e194c2806d0b697028434e3b9c02f59d`  
		Last Modified: Tue, 24 Feb 2026 18:43:22 GMT  
		Size: 49.3 MB (49293124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e22c0cca0928da3d2de6fd871bd926c0e88a444ffc6a9ca21f9feaed57ef86`  
		Last Modified: Tue, 24 Feb 2026 19:57:08 GMT  
		Size: 157.9 MB (157857099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4062761dfb817dda91578097f0a1cf2f496049ad549076c532ace5af4bffb559`  
		Last Modified: Tue, 24 Feb 2026 19:57:06 GMT  
		Size: 85.5 MB (85539359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9799a3c5dc93d7f96263502eb7a46f10daae4e964b8d0cc11728879e611655bf`  
		Last Modified: Tue, 24 Feb 2026 19:57:03 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d11f093454ba57e7c7a3240c9c31e4661653c322132c4752de8efb186ad4e8de`  
		Last Modified: Tue, 24 Feb 2026 19:57:03 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:dc50be6ff5857086e7ca7af9927ccb4bac47fab7548745ab9d60258f68037198
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7486686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c9bbb61c539ee0043ddd6f08cf4b72cbb74bb4bbec215a84631f3d2ce917d8f`

```dockerfile
```

-	Layers:
	-	`sha256:73db5a640191a1adfe27718832597d8192ca37272c88625dea98866f36a7d847`  
		Last Modified: Tue, 24 Feb 2026 19:57:03 GMT  
		Size: 7.5 MB (7470932 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0094a2fa185d734f12ec9d74b5bf8bd7f58332f2b06850ec22a8e4a73dfddeed`  
		Last Modified: Tue, 24 Feb 2026 19:57:03 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d626618f48a4dd36ab553515df88fb14f0ccd1c83a617d444f7bb7def6190502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.2 MB (291151418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50b6ce4b0bf119f991a475f1f628bd994c9dc6f829cd4ca6ae6efca597ef33fc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:07:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:07:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:07:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:07:09 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 20:07:09 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:07:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 20:07:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 20:07:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 20:07:28 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 20:07:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ac9148dc57ca750b09f3f3da6f16324e1a3b62432b2726734535ec610e1a9232`  
		Last Modified: Tue, 24 Feb 2026 18:42:56 GMT  
		Size: 49.7 MB (49652168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3c2babcea9c95c5cea64e8fe92565838e58109633e35fd24cf4a0aa32e4b0a`  
		Last Modified: Tue, 24 Feb 2026 20:07:54 GMT  
		Size: 156.1 MB (156133054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ffb1400fbb2342777c21a06b7afee59bc86e0228df7213bf01ae78ee77185d`  
		Last Modified: Tue, 24 Feb 2026 20:07:53 GMT  
		Size: 85.4 MB (85365155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dacc57f8e0151ee581b6b4192bafb9b953b4adefa1822ec423a47956bb90fe07`  
		Last Modified: Tue, 24 Feb 2026 20:07:49 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c491879418291419c3f7621db3b6a1e5ffd04129b73069c5e4f5b7258ef06c96`  
		Last Modified: Tue, 24 Feb 2026 20:07:49 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d3e77c6c3d32b633085c1b3261973ffc94b5d78153e7cd6ad4951fe1b74e6046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7493834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:306549dac139dabd5d660a023d7cfd1d145fc64375f88919c93a335c6133961a`

```dockerfile
```

-	Layers:
	-	`sha256:f078c9ed3ef978c86178f68d6e3355783f86b9ad688bc2d6a80595717ca0502d`  
		Last Modified: Tue, 24 Feb 2026 20:07:50 GMT  
		Size: 7.5 MB (7477962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a7d34bf03e3ceb227572656ba2f180b0885e905b1b7fb0e403f1e92435ab21f`  
		Last Modified: Tue, 24 Feb 2026 20:07:49 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:4886196d09a8d59dc1fcf124d1a0488961d041c4710f35102de967c079e3cf99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.0 MB (302047821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ca7366815145bccf2555372ca191d4e0bc78385df6b76ca7622f8460925cc24`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Wed, 25 Feb 2026 02:08:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 25 Feb 2026 02:08:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 25 Feb 2026 02:08:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Feb 2026 02:08:05 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 25 Feb 2026 02:08:06 GMT
WORKDIR /tmp
# Wed, 25 Feb 2026 02:13:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 25 Feb 2026 02:13:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 25 Feb 2026 02:13:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 25 Feb 2026 02:13:21 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 25 Feb 2026 02:13:21 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:468eb7cd0e9ceb9e5b1c4c9daadd36c2fd1f1ee82c667dc1a7d70fa95600a20f`  
		Last Modified: Tue, 24 Feb 2026 18:45:11 GMT  
		Size: 53.1 MB (53112261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e03e689c06567c80a28fd472748594e5fc56bc0f3f151ccb3aa20e431739eb37`  
		Last Modified: Wed, 25 Feb 2026 02:09:40 GMT  
		Size: 158.0 MB (157977516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f79cc86f293d07b392e8d87b837264e813d9a43fcf96a9c060c6289640c4f10d`  
		Last Modified: Wed, 25 Feb 2026 02:14:03 GMT  
		Size: 91.0 MB (90957003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6906f65154c9b8aee55893b3e8365571dd31bbabd8f062b9490a9ac50016ef71`  
		Last Modified: Wed, 25 Feb 2026 02:14:01 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb14243658686ee8cf7275da6ede33dac04a8afb5ec3507c84f6fc46695ee800`  
		Last Modified: Wed, 25 Feb 2026 02:14:01 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:971a28c103d2a8e72750598e9c2923d1958239aae3d2d515ac093d07cba5c144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:526e31dd1ce23f62026bf702fd462eea9c110b59e32b16fc55a849ee0e9ef360`

```dockerfile
```

-	Layers:
	-	`sha256:145f83e61838ee03aaa6dc21b7681af483227fef7f32a291f8088e94d661d139`  
		Last Modified: Wed, 25 Feb 2026 02:14:01 GMT  
		Size: 7.5 MB (7475353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc2544b81879b90c00344b3d90346b31422ec325fb5baca111c4c25e12b6d4e2`  
		Last Modified: Wed, 25 Feb 2026 02:14:01 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:34de855c4ece67729a7a560a1900ba876713b0ef0203e4a17f279033e89c9fea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.4 MB (289419790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7178323b6c1f5057f36878ba0f13b1a1a110eb4ac43538aca84ec639773dd9a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Wed, 18 Feb 2026 10:57:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Feb 2026 10:57:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 18 Feb 2026 10:57:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Feb 2026 10:57:54 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 18 Feb 2026 10:57:54 GMT
WORKDIR /tmp
# Wed, 18 Feb 2026 11:20:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 18 Feb 2026 11:20:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 18 Feb 2026 11:20:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 18 Feb 2026 11:20:54 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 18 Feb 2026 11:20:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:618efd37f74728f7dcba60c231fad7f2d777dc65e4da32d0adae5e032e1fd125`  
		Last Modified: Tue, 03 Feb 2026 07:13:10 GMT  
		Size: 47.8 MB (47776763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fe4d1ae6c02473cb929f0b7a5e682926ce210e0d69a3b3a3ac5e83f0da0871`  
		Last Modified: Wed, 18 Feb 2026 11:04:21 GMT  
		Size: 157.2 MB (157216908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46abe3866fe6b1fd3530ec6f427dd59e7469529270c35569f4bc6f2082f7562`  
		Last Modified: Wed, 18 Feb 2026 11:25:21 GMT  
		Size: 84.4 MB (84425071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb65cb2834f9255cd876d390cc84f3ab450d1f8c2aa9835e3cafa17b5e06c9a`  
		Last Modified: Wed, 18 Feb 2026 11:25:08 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfeb33026f79f83c576842b115779da4b3fb90404cbb36dd8fd0ff351a972694`  
		Last Modified: Wed, 18 Feb 2026 11:25:07 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6500dfab5219a0fd7932a8cd8cb1b9d40b58ad6ad04533d616609c42acbe33ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7474648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24816898f1bff0424767a8b692ec3eed6efd6b3c3dc42064e5c8d2c8fae75ceb`

```dockerfile
```

-	Layers:
	-	`sha256:4505cc2eab4a1ca6848809acadd6647efd46a7cabfceb069927308e375df16d4`  
		Last Modified: Wed, 18 Feb 2026 11:25:10 GMT  
		Size: 7.5 MB (7458847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc7052925800208e5c7ee6008abb1c5e16fede4459aa9cb9ebd99de21ab11d3a`  
		Last Modified: Wed, 18 Feb 2026 11:25:08 GMT  
		Size: 15.8 KB (15801 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:30e9fda2d6328e8f494d5c1e200920b84818e13d0dc7c5b70b3041278ab08531
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.0 MB (282975119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba8b3c0e2d586f5ca1c720ad7333e01349ff98dd611fc4be4242722056cd7319`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 23:22:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 23:22:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 23:22:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 23:22:38 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 23:22:39 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 23:23:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 23:23:14 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 23:23:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 23:23:15 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 23:23:15 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:aba9aa950add2749194487d5c63a3069af6daf9dfe54d80cfbe32bfa7a5faa07`  
		Last Modified: Tue, 24 Feb 2026 18:43:53 GMT  
		Size: 49.4 MB (49354534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13ddb44bc4e23c845d8416452a0b531a57cc933f0df6fb076c886b4d9472f68`  
		Last Modified: Tue, 24 Feb 2026 23:24:01 GMT  
		Size: 147.1 MB (147105302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014d7634ca5a024309f9aa0ec6710eaf962f1beb1485cf8e113a952bf35e02e8`  
		Last Modified: Tue, 24 Feb 2026 23:24:02 GMT  
		Size: 86.5 MB (86514241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ebd50ec3382952a9273a90652c132a6acd0d810da3e1afed0738916d103f80`  
		Last Modified: Tue, 24 Feb 2026 23:23:59 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad630fb8f295e78fa8d2cdba57e2f158f49b86e19754edb0edce384b8b78ef3`  
		Last Modified: Tue, 24 Feb 2026 23:23:59 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3986d9b793ae068dd0c041b8dfd5d599c37a54119ad89df38ba337f7fb037caa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c11cc78882e719b5d97356de6a912f00d2ca0f178e748688a9004fbb1ec726`

```dockerfile
```

-	Layers:
	-	`sha256:a648b22becd3a920ac02f960835d0ad31117ae43282afd3330344b4163e361f5`  
		Last Modified: Tue, 24 Feb 2026 23:23:59 GMT  
		Size: 7.5 MB (7466854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caf0b9493ef072cb4313a05ba1fed54c8d2c57b2eb9a21dc253178483f8f595d`  
		Last Modified: Tue, 24 Feb 2026 23:23:59 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json
