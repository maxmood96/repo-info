## `clojure:temurin-17-trixie`

```console
$ docker pull clojure@sha256:c3fba37437ffc9f9e119225e1dbd6cb9165111c494ee04866a7f7c119870facf
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
$ docker pull clojure@sha256:f972ef89213be6db3edcd029b692667d83dd27afeefcbdd2620c8d6b6a73face
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.1 MB (279144605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab5eacf6eae2764a809f1a74be9383d631e43f14d060fd09b8f21968b0125f5c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1745798400'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f8c8542523ef5c08ca9bd5ab7d7265d12930a45ccc7c8364e909fde03c894479`  
		Last Modified: Mon, 28 Apr 2025 21:08:35 GMT  
		Size: 49.2 MB (49248239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88a9e6e9439e1e71dc15cf1210c05634bbd063835a1bd6b1be16383dd15dd8c`  
		Last Modified: Tue, 13 May 2025 17:53:52 GMT  
		Size: 144.6 MB (144634958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ec079f30e0f37a49ae8ce9681bdf2823d40e6924f94c6c6be3ba9ccf369541`  
		Last Modified: Tue, 13 May 2025 17:53:52 GMT  
		Size: 85.3 MB (85260369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2fdd627fd48d47f4e159533fba8f5170d7207873a33aac6317caeb3da6b8ff`  
		Last Modified: Tue, 13 May 2025 17:53:51 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8a0cc5693c3708f664bdc93b254074495f60174bed244f19b0f507b0357628`  
		Last Modified: Tue, 13 May 2025 17:53:51 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:81d880547029b5bd07a6145753422845f46878d4e0106443201578e6b4313557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7284966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9103d5ca2229196239cf0944647b0a25556012b5443fd255f84939fd2dc702b`

```dockerfile
```

-	Layers:
	-	`sha256:aa10e12f731ab034de1d1be583bc5df784f0311373dce3f4d95a2df9e5ac3ee6`  
		Last Modified: Tue, 13 May 2025 17:53:51 GMT  
		Size: 7.3 MB (7269169 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77acafbd2b76f75c2ec5266b1524f420245228a62f0037ca693f80c1872590b5`  
		Last Modified: Tue, 13 May 2025 17:53:51 GMT  
		Size: 15.8 KB (15797 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6402e11a2d3ec092a1931395f695778a59414813fee8af963cb7a56ca693d635
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.3 MB (278310164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19615e32c02d5c9c7b984a3c9dc0e3bc22e00d773de5fec8cfd22fba70b0577c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1745798400'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:288a1cecb0ea762427d39b072c1ca965d193e927e04da652f7b21eb12e9b2acd`  
		Last Modified: Mon, 28 Apr 2025 21:23:23 GMT  
		Size: 49.6 MB (49624118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b282e0ac6bfae3681aa56a27479878cb17caec1c03eac0e2edb7ee5cb06808d`  
		Last Modified: Tue, 13 May 2025 18:00:41 GMT  
		Size: 143.5 MB (143512641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef55628f8b5c6edcca9fddd776a947cd72c252c67307d4c5f6b7fcf1e3550e2`  
		Last Modified: Tue, 13 May 2025 18:02:36 GMT  
		Size: 85.2 MB (85172364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8be010195df5db74d0dbf792669e22ef3037f67480a5a81a8971e18402ed08f`  
		Last Modified: Tue, 13 May 2025 18:02:34 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0955237417bf5420fca670cb5cbc1475f52e66307da4d77a6fddbf1894be7026`  
		Last Modified: Tue, 13 May 2025 18:02:34 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ed14401a090c1d142099290c378c0acec0537c9c5b3f88b8989a958f349b7687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7292114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e83a94754e5cb1e76d364cf613d48bd5a1b3e43833d0a6796efe02bdb827cce9`

```dockerfile
```

-	Layers:
	-	`sha256:43ff7acfbf8661adba5a826cc4f39d591df26e842803fbf917c83e60bb677487`  
		Last Modified: Tue, 13 May 2025 18:02:34 GMT  
		Size: 7.3 MB (7276199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:021a09065e425efa872347a60f56817b2f9cc2b9efe64ed7ec0356b8fada8697`  
		Last Modified: Tue, 13 May 2025 18:02:34 GMT  
		Size: 15.9 KB (15915 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:d5c57553a40c856288b5a1962d388ea5b2c03ba36e801c894ef16045e630eaf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.1 MB (288096888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dbff646f624a68cd163f1066d8847b055c358ace56ed1e2a249c436cd988d07`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1745798400'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:03ebb30bb37cd398ea8ab1a268c301664089cf5a54d23466e4338782afb5f9cf`  
		Last Modified: Mon, 28 Apr 2025 21:25:28 GMT  
		Size: 53.1 MB (53072552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae552af9b4a5f2c0ec434558439412e3b3de2a024f98aa1612023e6c631f846`  
		Last Modified: Tue, 13 May 2025 18:57:26 GMT  
		Size: 144.3 MB (144280526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f989255aa15b3273dc7a86d27de11aff288e7510b38437bef7657bd03a2ebe`  
		Last Modified: Tue, 13 May 2025 19:07:43 GMT  
		Size: 90.7 MB (90742768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5efd8769d419348fdc2459680eaffea692c4c34e5d5c49d86b2f97954c8a9fe`  
		Last Modified: Tue, 13 May 2025 19:07:40 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f209e02eb2ebd4a135502ca8f04ef0243b3cb823da62d1ba5ef78ee8d375be`  
		Last Modified: Tue, 13 May 2025 19:07:40 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:5a99019654b69a2120b0ba7a433be11c5572a2618fe86f006599d3509f086403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7289267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23ecff4ff8a3e8ffa0817536360500df08cb457ae6071e44c48be17368b194f7`

```dockerfile
```

-	Layers:
	-	`sha256:b465b3a4f88a28f7301058b63d4e7604c540cb69b64a8174db3cabc50795bcd8`  
		Last Modified: Tue, 13 May 2025 19:07:40 GMT  
		Size: 7.3 MB (7273422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97313bf24d02a26ce81d681c8371106965c7a58aa324f10290bd25847b456e99`  
		Last Modified: Tue, 13 May 2025 19:07:40 GMT  
		Size: 15.8 KB (15845 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:0d95118fe2158eb034a8c69c11cdbab01725b0a5e99cb86d9b38b8884fd9b9fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.4 MB (270445913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b07e2c4248350553ab43151f1ef7d32d18e66ddd0ffd6027a392187bf94d8237`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1747699200'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c83c5fa20952cc8610d790073e97537e7832127593042fa9c620fa910fe6f6b9`  
		Last Modified: Wed, 21 May 2025 22:36:51 GMT  
		Size: 47.7 MB (47731411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa6d609f781d308e56eefcb1110f30e4afe9c0d5fb3da3186df488fb49f4424`  
		Last Modified: Wed, 21 May 2025 23:49:13 GMT  
		Size: 138.5 MB (138492686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1dc90a3edb914ebcf7e51b0b2213312fe85db336ba91f194c1390c44863489`  
		Last Modified: Wed, 21 May 2025 23:49:06 GMT  
		Size: 84.2 MB (84220778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8839e780573c0e2db9214f35caad4d5f66081b03f3db6cfc42dbaf709fee57d7`  
		Last Modified: Wed, 21 May 2025 23:48:54 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a164e59b725eaa0f553d2f8e581adba111f21f18b439cab3c9b8a003383b2be`  
		Last Modified: Wed, 21 May 2025 23:48:54 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e89cc61b8ac40a0969802f2c53c6448bf02adfbad89521238e7ddf47bbc10e1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7320253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68b9180394b8562a4366bf52ee79bee165701577f17cac7a72048b3bf59ac5a1`

```dockerfile
```

-	Layers:
	-	`sha256:fde98592b179e3f9433af1e2c013e955d5fc1f5fe9b6fee2ad30ee51c5e1de68`  
		Last Modified: Wed, 21 May 2025 23:48:55 GMT  
		Size: 7.3 MB (7304408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9df34476e8d4efac22e7ba917337d14999bf37bc290c9de2bb7dc2bd334a73a`  
		Last Modified: Wed, 21 May 2025 23:48:53 GMT  
		Size: 15.8 KB (15845 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:39f0ea2ad2807610b0cba65bb88dadd2bbe7662693a779c2595f78bc22c3b074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.3 MB (270330437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09f9948b54af4cf0ddb339d855efb2e30bd876cb417ef8a4413557066b256ff4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1745798400'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e1ec3b1570f7d822c5a6aa013529484429ad99bde8495d827b56c3603992fd3c`  
		Last Modified: Mon, 28 Apr 2025 21:11:06 GMT  
		Size: 49.3 MB (49316646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ca100b33a26d036b967727026db8398303b1b8542c4f1f20bacfc893669267`  
		Last Modified: Tue, 13 May 2025 18:13:20 GMT  
		Size: 134.7 MB (134673562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0af6ded15fc5acda748d2061bb2c3877d9a328b2e82329e55dd9d2ebc85c0f`  
		Last Modified: Tue, 13 May 2025 18:19:13 GMT  
		Size: 86.3 MB (86339187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a925b050d4517359e1b38270bb5381c506958bb99deb7ad0debe735fdae1414`  
		Last Modified: Tue, 13 May 2025 18:19:11 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28100c07e910a3f0d63a87f210ac5ebb6920fb4181e6d896efddc5615fadf52`  
		Last Modified: Tue, 13 May 2025 18:19:11 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:86e20e3dbe859e60dffc8023409e3a778126c4c83021f8844c4948ca694ce8a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7280888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ebf2286df741f4184b2b4870f751bacae3478fa5a76d70b2a7515bf384f5eb2`

```dockerfile
```

-	Layers:
	-	`sha256:4e76bc1ae969668d95eb867199b04f27dfe47456f491454d8b3ef9d15303f4db`  
		Last Modified: Tue, 13 May 2025 18:19:11 GMT  
		Size: 7.3 MB (7265091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:051fe41382a6c085b45f6b870e66bb9ff2612f7f1eb903db3aaaef162b490b49`  
		Last Modified: Tue, 13 May 2025 18:19:11 GMT  
		Size: 15.8 KB (15797 bytes)  
		MIME: application/vnd.in-toto+json
