## `clojure:temurin-24-tools-deps-1.12.0.1530-bullseye`

```console
$ docker pull clojure@sha256:c6565f166d5010b7aaf5d448cdd4118c5f748f0de62acbf9dffb6c2f153483e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-1.12.0.1530-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:4ef64b35097de6babfc2ee4254d157b024d80422d51db9de42d9b92505d7b553
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.1 MB (213101955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8691a6c4ca1a6000f076a61c99eab755098b3ed67869aee5ae334624a05a475e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
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
	-	`sha256:54107f2de180b7b6e9f909d2f1c6c18e10c700a6bd80a035d931768b06bb2905`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 53.8 MB (53750195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671b36b118546778f621aff30aa94605755a96eff7bffba6067cd81b207581fd`  
		Last Modified: Wed, 21 May 2025 23:34:53 GMT  
		Size: 90.0 MB (89952021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6713e04a05b4abf38dd52c0e7591ab38b1a0505cf8180be360def39529acd769`  
		Last Modified: Wed, 21 May 2025 23:34:53 GMT  
		Size: 69.4 MB (69398700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5a848b3b1514df49c809a565bbb6d673cfa737c286752c7d3697eff7eb583a`  
		Last Modified: Wed, 21 May 2025 23:34:50 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16736939811007dc3142502f48ff80ddb308aa98060cedc5c0fbe235af5ce71`  
		Last Modified: Wed, 21 May 2025 23:34:50 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.0.1530-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:7cba900626778ffcfc5b164f9e06271be70c6c0d76fb0cd5fe421ef4cfb5fc81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7221050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fc2fe3caf6e40abd7fa1a17567c66b70dbfc3674252c7c7e9a09786a4615bd8`

```dockerfile
```

-	Layers:
	-	`sha256:418ff3b21047cc3c8fb3fb43557967c6f085c89a783628e29e61b6c4fb61f490`  
		Last Modified: Wed, 21 May 2025 23:34:51 GMT  
		Size: 7.2 MB (7205236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fd980aad97cc96b63f5a476d406598e686715b0e24e6b74a597f29158d6c682`  
		Last Modified: Wed, 21 May 2025 23:34:50 GMT  
		Size: 15.8 KB (15814 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.0.1530-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6195d24e024ffbd9951a794b9307a7475b69a0c02f8a8bbd6c63c3fb0f0856a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.9 MB (210867847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aaf2a9a2a44c0ca81b5fff913c07d359097cb3ab61dee9b9f4a0c8da45f5b88`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9ce0153b823c3af508e9c8a003aa35daca140e8f4578ff2a451ac20469ea739a`  
		Last Modified: Mon, 28 Apr 2025 21:20:53 GMT  
		Size: 52.2 MB (52245979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea499e9a6440c89518277b243ca49b2d9515371f555e0f6fb5ae8bfd73d843e6`  
		Last Modified: Wed, 30 Apr 2025 01:51:08 GMT  
		Size: 89.1 MB (89091271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d647400935d43344d8fd0006b65eedc14a5dcfdb1a2e671ba2461d208eb2f1`  
		Last Modified: Wed, 30 Apr 2025 01:51:08 GMT  
		Size: 69.5 MB (69529557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aefe9a46362a5361e8561468f5f372b043300812c3e534642560ecf59dfc2adc`  
		Last Modified: Wed, 30 Apr 2025 01:51:05 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1ba61a959a7027eabf5c73312b56c2171dd659a136e3d537f8ccd2541f7752`  
		Last Modified: Wed, 30 Apr 2025 01:51:05 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.0.1530-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:1585f09ba112fc761f7ab02159e235b114cb33bc2b726b0f8cadf52d25b59986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7178229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cedf174e47155ca9dabadbc76b6941be233d17a29d25c04420bcdea448cfcb6`

```dockerfile
```

-	Layers:
	-	`sha256:f243e2a15ef98ff6c56650efc4b6c98de1c855e57fae7e7c021b0f4a92ffd37c`  
		Last Modified: Tue, 06 May 2025 00:49:53 GMT  
		Size: 7.2 MB (7162297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ff35995bfce347a4faf86a243040da484b7569c236c71d624e26d1cb9400c17`  
		Last Modified: Tue, 06 May 2025 00:49:52 GMT  
		Size: 15.9 KB (15932 bytes)  
		MIME: application/vnd.in-toto+json
