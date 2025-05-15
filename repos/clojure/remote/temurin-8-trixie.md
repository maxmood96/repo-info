## `clojure:temurin-8-trixie`

```console
$ docker pull clojure@sha256:2221eaebd66fc867c2828fc9ee628be268ae48d6f31c3a079d3c006c4ac5e138
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
$ docker pull clojure@sha256:9bcd7f11d26c2a458870683db932fed9ccf52fd626da4ba554324954328eebe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.2 MB (189225196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3107a193dc7e7fd2f053cfe3a867b4f24f23f91f9fba7299a514c742f635677f`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:f8c8542523ef5c08ca9bd5ab7d7265d12930a45ccc7c8364e909fde03c894479`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 49.2 MB (49248239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de0df3419df1709454d7a8ce2b3f5fa0b67813b1cc62007f46259b12b7f469b`  
		Last Modified: Tue, 13 May 2025 17:53:35 GMT  
		Size: 54.7 MB (54716179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad5e162ec491b2eef869c8635f8add3dd9537c31783f2e5eaea44de09f029815`  
		Last Modified: Tue, 13 May 2025 17:53:36 GMT  
		Size: 85.3 MB (85260131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36019535f684e5e88f39b11ab33f9e1e0359c4b848d9868b33225352ed30c3c9`  
		Last Modified: Tue, 13 May 2025 17:53:35 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d6cdb4c2526bf920384e775517e62b7f443c6ce57215d8b0b0fa3fa3cba23351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7404991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78faa6e79257b754acdaecce58c41c40ef0c671896e90d5b164fa69ac4a6b10a`

```dockerfile
```

-	Layers:
	-	`sha256:b593b566eb85adc7cb9a70304876d3c396cd9653a5d21275715bdd307102234c`  
		Last Modified: Tue, 13 May 2025 17:53:35 GMT  
		Size: 7.4 MB (7390779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0203e7fcf7d32bf6de2cdbd690e6e739c45a50483b0a3a4efb6f1438a8ad4b5f`  
		Last Modified: Tue, 13 May 2025 17:53:34 GMT  
		Size: 14.2 KB (14212 bytes)  
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
		Last Modified: Thu, 08 May 2025 17:11:50 GMT  
		Size: 49.6 MB (49624118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d406b9ad14858667774dca77e79c17a0e68ce55fbb312cf3ac281f2270103a`  
		Last Modified: Tue, 13 May 2025 17:53:32 GMT  
		Size: 53.8 MB (53830516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
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
		Last Modified: Fri, 09 May 2025 00:28:48 GMT  
		Size: 53.1 MB (53072552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1676143d0c211519b773b6521adf180c811c58f3f9a5d2485e130a3de71661fa`  
		Last Modified: Tue, 13 May 2025 18:03:53 GMT  
		Size: 52.2 MB (52167968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
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
