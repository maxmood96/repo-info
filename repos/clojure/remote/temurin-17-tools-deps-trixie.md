## `clojure:temurin-17-tools-deps-trixie`

```console
$ docker pull clojure@sha256:3722ae7b9c16126204c43c5e1f980421efae75b30dfc854e8075914cb9aa09c1
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

### `clojure:temurin-17-tools-deps-trixie` - linux; amd64

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

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

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

### `clojure:temurin-17-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c2552dd7b4cdc195481dbe29801dff908ca96eace802a33501ce15479e66a25a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.3 MB (278307428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7588c0bc1eecec0e478cf1674e537b78779a73067d57c2b6a73bbb91a73124b4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1747699200'
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
	-	`sha256:397826b9fe635f12caff1a603eb12c37426a5b3dc563e0adff2debff0c68a6b0`  
		Last Modified: Wed, 21 May 2025 22:31:07 GMT  
		Size: 49.6 MB (49618294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c62834179478a30cc196384b5343ea2eea0a3a82d12d33dd77571aa1f847b4`  
		Last Modified: Thu, 22 May 2025 08:23:18 GMT  
		Size: 143.5 MB (143512648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766fd0a963396468c4f388bbe8b3668e86c8b7c96ea9c602ea3b334b04befe28`  
		Last Modified: Thu, 22 May 2025 08:27:53 GMT  
		Size: 85.2 MB (85175445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5ff6e7c5cf332d915afd34b508140ce4fda8d305f0e6b436a29d1a170018a5`  
		Last Modified: Thu, 22 May 2025 08:27:50 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9999c3185cb70774d4a6914f9df451cb1007051d537b4799c72aa4144abf3e7`  
		Last Modified: Thu, 22 May 2025 08:27:50 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:4c74c7a5f530253ebbadbf4f5183fe36a6a037ccde7e9666777eede9da2a924d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7341361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5d98e293703d0c3b78b145442bd3f2f8e43fcb7bf047987ceca9cccb975c581`

```dockerfile
```

-	Layers:
	-	`sha256:325a5d9562e02c493aee0ae689f40b7f40cd7d592271d26860a33ddd9d6fb4a4`  
		Last Modified: Thu, 22 May 2025 08:27:51 GMT  
		Size: 7.3 MB (7325446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2167b11b65af93629fba3d981ab0105d776d3f8fec9f9ccb6573ae21f52a3e42`  
		Last Modified: Thu, 22 May 2025 08:27:50 GMT  
		Size: 15.9 KB (15915 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; ppc64le

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

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

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

### `clojure:temurin-17-tools-deps-trixie` - linux; riscv64

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

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

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

### `clojure:temurin-17-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:3d44f493c0d6e4a8888a441e3b1043c23b0c3926de4b3378ed27054d58848eeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.3 MB (270336957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c60b41a0c7691f216a6761dfe26e67d4b1568b2d2fa2183637e2c19aca295c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1747699200'
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
	-	`sha256:71c8524b25c34592c256fbae9045d0ade48f5e9889d37c5b2190092fa9017d48`  
		Last Modified: Wed, 21 May 2025 22:31:46 GMT  
		Size: 49.3 MB (49322227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6b8105b30bce6e4fe650cddd98c90e44cb61cd2de3f9d9d5f8742105b115b4`  
		Last Modified: Thu, 22 May 2025 03:51:43 GMT  
		Size: 134.7 MB (134673562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec152d9ec0d7e61571189db7d2c788709b5f9b51446877c6e12b5d2631e709e`  
		Last Modified: Thu, 22 May 2025 03:55:41 GMT  
		Size: 86.3 MB (86340130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3db57d78bcec71c5c57a093d3b98b58cf992d2368036c75e402d2e70678965`  
		Last Modified: Thu, 22 May 2025 03:55:40 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2455796dc9eb303277c64d50d5c3c515da1bd0ee0cafb9fcc33bb80d0ca6117`  
		Last Modified: Thu, 22 May 2025 03:55:40 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:11af5da17b89142feabfca3fa8b999384c0bedfdbc501335d2c73f51e70f0e97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7330135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8671bcfb0d4c962ba2b1c57d3fc8e749441b218f9ee8dfad66b366eb0a4b45d`

```dockerfile
```

-	Layers:
	-	`sha256:46aa5e6a8b511b5ede4b151604ab8684c2108ac3ba0cf553763d47a7e45f97ba`  
		Last Modified: Thu, 22 May 2025 03:55:40 GMT  
		Size: 7.3 MB (7314338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd626822e62ee984c12dc29e89f6a85a8a6409fab123f2a7c590f6424d949b30`  
		Last Modified: Thu, 22 May 2025 03:55:40 GMT  
		Size: 15.8 KB (15797 bytes)  
		MIME: application/vnd.in-toto+json
