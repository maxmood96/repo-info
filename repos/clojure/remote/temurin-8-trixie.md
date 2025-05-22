## `clojure:temurin-8-trixie`

```console
$ docker pull clojure@sha256:8c252aa354a495e508adbb9f6134eb4f9f6be6977aee84a99883527a478653f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:750ef0b8f6850f047a1aed8841b431471fc1239efa7a09f10f0c301e2de37df2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.2 MB (189222772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a04c99e7e0361761989cda006714648ff51ab8461410f45e15fc739349eb0b8`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:b8364400c35b20e530ea76455b7a73bf615b17d9d6734e0c2539034d9fe0bed1`  
		Last Modified: Wed, 21 May 2025 22:28:00 GMT  
		Size: 49.2 MB (49246908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33ec3b2cf56ad31185f65db380fc5018ff1fee91bd1a06a168aa95e9bb13dbf`  
		Last Modified: Wed, 21 May 2025 23:31:59 GMT  
		Size: 54.7 MB (54716171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37463d9a4e86dbc0ee4cd59586f8bb91d9c45b0b6d2a2c2a45b34d4faa12fefd`  
		Last Modified: Wed, 21 May 2025 23:32:02 GMT  
		Size: 85.3 MB (85259049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98d76fae2e764566deb297391bd6a09339ca13aaa7f80948772185580b9f20a`  
		Last Modified: Wed, 21 May 2025 23:32:01 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c989e08cb705ab6a9e71a71d257779f34d7041a928a7fb24f88ed05e60e45d89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7454239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38039b2efff212965e1c25b27c2e966edbbc4c8320b8548525a7cde82701b9f2`

```dockerfile
```

-	Layers:
	-	`sha256:3fa23f6675953e2110872ae65c76c258feb72fe3f7aba3f3514df22c8d2bedaa`  
		Last Modified: Wed, 21 May 2025 23:32:01 GMT  
		Size: 7.4 MB (7440026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1cd991c035cddfdfbeeed2c711d19046e351391d3e2cb33b5b74bf6644cdea3`  
		Last Modified: Wed, 21 May 2025 23:32:01 GMT  
		Size: 14.2 KB (14213 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:080438626a6125542d5f738076ec26d8f99899e661584b996d45cc4615c49f2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.6 MB (188627812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ccdc1153a5e4aab1d477d50e14920ea943cd24023c167cd94e34399c9d294c9`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:288a1cecb0ea762427d39b072c1ca965d193e927e04da652f7b21eb12e9b2acd`  
		Last Modified: Mon, 28 Apr 2025 21:23:23 GMT  
		Size: 49.6 MB (49624118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d406b9ad14858667774dca77e79c17a0e68ce55fbb312cf3ac281f2270103a`  
		Last Modified: Tue, 13 May 2025 17:53:32 GMT  
		Size: 53.8 MB (53830516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba52d71adfa51e17a5c6e62d5169cb03bd1909fbdaa43295815753885df08c60`  
		Last Modified: Tue, 13 May 2025 17:55:24 GMT  
		Size: 85.2 MB (85172533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54cbb9eecfacb3a6ebe07da3280bbb2c7cb8f91d5221995400cc2f8c2550f821`  
		Last Modified: Tue, 13 May 2025 17:55:22 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e5785ff606f865e16f60af69d74a9ad9015be097c02b4d5e20f2917546edc682
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7412838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cd39b5308a0e84535528d626f1a59e4f3cefbabf988045cb23bdfe76cdd8096`

```dockerfile
```

-	Layers:
	-	`sha256:ba18ac66d2fae0ac271d47f9fb93b02462ec4cd34d14efce002eaf9f16387113`  
		Last Modified: Tue, 13 May 2025 17:55:22 GMT  
		Size: 7.4 MB (7398507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c8d9368239bfc7c66c34aa7f1ff10e90a381dc2432d3e6b625d516882cf9d6f`  
		Last Modified: Tue, 13 May 2025 17:55:22 GMT  
		Size: 14.3 KB (14331 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:5704032e65216da46cd2e57c16f4998250b446f0cb45ece577b58f7b951638d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.0 MB (195984221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27b888fc7f8f1c9b01611f9bc445b34a056ed6638801f48d357c07c659fb5fd9`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:03ebb30bb37cd398ea8ab1a268c301664089cf5a54d23466e4338782afb5f9cf`  
		Last Modified: Mon, 28 Apr 2025 21:25:28 GMT  
		Size: 53.1 MB (53072552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1676143d0c211519b773b6521adf180c811c58f3f9a5d2485e130a3de71661fa`  
		Last Modified: Tue, 13 May 2025 18:03:53 GMT  
		Size: 52.2 MB (52167968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd6faed69ea0997395430df706271b547104fb40b48a4a4f64f227149f10b866`  
		Last Modified: Tue, 13 May 2025 18:17:39 GMT  
		Size: 90.7 MB (90743056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f374b639125f9ab855b32c0f9005d7824df010f3ed7efadf15eec5fd2a44bc6b`  
		Last Modified: Tue, 13 May 2025 18:17:37 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:fe75ca0158bf46456b0390c6d5cf2190b49e166a27509a1b0eda802ca27cdd77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7409886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f953af4c18dca8dfc187087aa7900bdc6787d3413e85b141112f7c338a33384c`

```dockerfile
```

-	Layers:
	-	`sha256:f72a29f92366871f4678edef38e5952a8fcf7b313edb1e37d38ce99e037b5012`  
		Last Modified: Tue, 13 May 2025 18:17:37 GMT  
		Size: 7.4 MB (7395625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef7f256a5e8b6c2110bfc3633d1640672bd83d38207b811713a38eb8a52e2dce`  
		Last Modified: Tue, 13 May 2025 18:17:36 GMT  
		Size: 14.3 KB (14261 bytes)  
		MIME: application/vnd.in-toto+json
