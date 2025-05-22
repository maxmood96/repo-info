## `clojure:temurin-17-tools-deps-1.12.0.1530-trixie`

```console
$ docker pull clojure@sha256:3e3b8391b30a8ddf18c82b18f872b594919aa938c00c04e0da03c028441644bf
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

### `clojure:temurin-17-tools-deps-1.12.0.1530-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:7e9a71aae593e8e5ae2643bf7cab88adb774b7666f986c1b587fa358715093e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.1 MB (279142035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f001eb2cfe22b4ee0268f890054a501e89ea84623e952ee72e5bbaa5649ba8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1747699200'
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
	-	`sha256:b8364400c35b20e530ea76455b7a73bf615b17d9d6734e0c2539034d9fe0bed1`  
		Last Modified: Wed, 21 May 2025 22:28:00 GMT  
		Size: 49.2 MB (49246908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2eece07e8c327e1ad3bfedc76eb95750755b7e5f443a84250b086221c7f5e09`  
		Last Modified: Wed, 21 May 2025 23:33:13 GMT  
		Size: 144.6 MB (144634954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3449698f2e138e912b2edd7ffc3b4e6b072fe2a7fe3539e5474c5bf2cef0b27`  
		Last Modified: Wed, 21 May 2025 23:33:13 GMT  
		Size: 85.3 MB (85259136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6e3ba0d70b0fa0d89f0b8905508d30eb8a24e04ee795f380941abbfc924df94`  
		Last Modified: Wed, 21 May 2025 23:33:11 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617f05fc9dd126210867b1459260ba350210a9f1e3183cc2fe7fd44ade9c3f9d`  
		Last Modified: Wed, 21 May 2025 23:33:11 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1530-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d3f66fe9ff56e73ac3a363b40864ea1fe1919e5e3312f10d9eef61af30392b33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7334212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abb92aa151e99f3ef76c81626cb6ca8e474c46affb76822cbcb0e012d9bff28c`

```dockerfile
```

-	Layers:
	-	`sha256:094bdc8458bbce1811c9ce268646ec5d3c95a5167a65f2e6ada673a858cb68fd`  
		Last Modified: Wed, 21 May 2025 23:33:11 GMT  
		Size: 7.3 MB (7318416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d45a7e9d829267945467da704d0bd113d62b4e8dca93b9930755b73eb27372f`  
		Last Modified: Wed, 21 May 2025 23:33:11 GMT  
		Size: 15.8 KB (15796 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.0.1530-trixie` - linux; arm64 variant v8

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

### `clojure:temurin-17-tools-deps-1.12.0.1530-trixie` - unknown; unknown

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

### `clojure:temurin-17-tools-deps-1.12.0.1530-trixie` - linux; ppc64le

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

### `clojure:temurin-17-tools-deps-1.12.0.1530-trixie` - unknown; unknown

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

### `clojure:temurin-17-tools-deps-1.12.0.1530-trixie` - linux; riscv64

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

### `clojure:temurin-17-tools-deps-1.12.0.1530-trixie` - unknown; unknown

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

### `clojure:temurin-17-tools-deps-1.12.0.1530-trixie` - linux; s390x

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

### `clojure:temurin-17-tools-deps-1.12.0.1530-trixie` - unknown; unknown

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
