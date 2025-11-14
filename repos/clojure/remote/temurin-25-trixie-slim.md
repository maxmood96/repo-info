## `clojure:temurin-25-trixie-slim`

```console
$ docker pull clojure@sha256:2058a7a16e7d8c8108eaa8544a32b9fd5a72004542328ae01d510e3a51ff9e14
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

### `clojure:temurin-25-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ba4953991e0a1513b9504d0333917fc76506e957eda49119d3a57ff7c23ce6c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193819921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992c04ef7fc71bad65a84df14ab286ab59144cab61f9152f63446c66d3ae5432`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 00:56:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:56:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:56:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:56:28 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:56:28 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:56:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:56:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:56:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:56:43 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:56:43 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14639f5b1ab1fc571cf72da5641f86ccc2495bbe99a5997345ae45974cc2f596`  
		Last Modified: Fri, 14 Nov 2025 00:57:25 GMT  
		Size: 92.0 MB (92045298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec66ce1141c71dafafbf49820d737dc5790239a9c729324fedc93840cafcb665`  
		Last Modified: Fri, 14 Nov 2025 00:57:20 GMT  
		Size: 72.0 MB (71995479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eeae1395a3e4162c00e21e21b3943a8df7cfeac63eb7641eb756f7f2118d2a9`  
		Last Modified: Fri, 14 Nov 2025 00:57:10 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f854639459aef09b33d38926e92f598eb603205f85dcee04b72000cc718f48`  
		Last Modified: Fri, 14 Nov 2025 00:57:10 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cb0a47e573f4769dc3d98b8dbc43fb3c920f6538378e556fa2ba060bb9e13958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5224012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3265d08b9403c273694f93d95c6495145b3c46b173cf7bc4fc4d13aa72eac730`

```dockerfile
```

-	Layers:
	-	`sha256:d335c75fb480620e956b77e775e1dad978e4fe5e6466941559f117861b2396a9`  
		Last Modified: Fri, 14 Nov 2025 01:48:37 GMT  
		Size: 5.2 MB (5207519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3f5a28945d4c637f2bc2f57c9c8f9e59a52d5b32276273cb57ac83456f2cbbb`  
		Last Modified: Fri, 14 Nov 2025 01:48:38 GMT  
		Size: 16.5 KB (16493 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:30e1e1179d738b162ab197bccb5d4e8e905364f056fb4b8c04ff708efeff2476
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 MB (193004278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eadd3e566d03ec6c2534a4a5676638e4e09c429a4d70b4ee65a7c61d16d779bd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 00:57:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:57:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:57:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:57:59 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:57:59 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:59:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:59:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:59:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:59:16 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:59:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:262cc0685394031f6ff3f3d0a86490a12fae03ec5c20c9024d342feed10288dd`  
		Last Modified: Fri, 14 Nov 2025 00:58:54 GMT  
		Size: 91.1 MB (91052512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:355c8615e558d4dddcdf0b15c097fde287d1184fc02361f569ac890c7b29a12b`  
		Last Modified: Fri, 14 Nov 2025 00:59:47 GMT  
		Size: 71.8 MB (71808425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bdedd3b7d38e2f0d780fd269fa7a460471d2272e47950bdf66a2b60608364d0`  
		Last Modified: Fri, 14 Nov 2025 00:59:37 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56060fb4f5aae261acd42e9837568252414d7c1a668e7c81edbf1d865e1ad9d9`  
		Last Modified: Fri, 14 Nov 2025 00:59:38 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1c16ec4e1f1249a327c3c80b76a9b379a06565d399774884b1bf4487f27ec797
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0c0749230e0eef3f5bf866778d84d1a9638568f3f9b15753c8b81cb47387ed0`

```dockerfile
```

-	Layers:
	-	`sha256:aa42fd35590b97d7c6119ea3bfc23e89aaca709f5b4ee0f6489c3f16bb840740`  
		Last Modified: Fri, 14 Nov 2025 01:48:44 GMT  
		Size: 5.2 MB (5213309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d6f7ec8e3f23c7b182fbf07b877e9f1fd0d278b872cba0083ba5be3c6e48c81`  
		Last Modified: Fri, 14 Nov 2025 01:48:45 GMT  
		Size: 16.6 KB (16635 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:8dfe99059e2365cef24e0795b6fa6758fca09e2fc5dad7f8db251256317bed52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.6 MB (202606220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d861a832a30e609b248240c746eb896ca31cc4ad5d3011b441dd9adebce51ec6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 07:38:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 07:38:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 07:38:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 07:38:50 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 07:38:51 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 07:47:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 07:47:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 07:47:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 07:47:37 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 07:47:37 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e214a9e01b759d7b08b8557e73d24cd420e1a0095fd9ed8d25175ebdcd1470`  
		Last Modified: Fri, 14 Nov 2025 07:40:17 GMT  
		Size: 91.6 MB (91610774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a685c3f929998981bd1112d4ae7e64416134827ba1b58eaf37962c2fd940bc4`  
		Last Modified: Fri, 14 Nov 2025 07:48:29 GMT  
		Size: 77.4 MB (77395754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac77a9aaa7f5d3bbbea5c4e861120ad8cdbcb71e3bac76e462dadc1796631af`  
		Last Modified: Fri, 14 Nov 2025 07:48:22 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f7820c4b20251de4183002766cc167f976082225d4284944b84c0925a6403ce`  
		Last Modified: Fri, 14 Nov 2025 07:48:22 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:df1a2ce2421790daa9744d21e6b53e0d7363e71a5755b38c96f31fd7589ee69c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ac321e0bd899512da12552a5353f7f8790f21533f5678d8fbdf179e3f1cad9`

```dockerfile
```

-	Layers:
	-	`sha256:7c7a4ed56166a2f576e8f7f14165b0d806fcc32fb260ef146832f41e24fe66cd`  
		Last Modified: Fri, 14 Nov 2025 10:40:43 GMT  
		Size: 5.2 MB (5213200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b6b3e7d4d8042266a71b0e35f7c5e5fe27f4f634ad2cf2204c165ca232ec3cd`  
		Last Modified: Fri, 14 Nov 2025 10:40:44 GMT  
		Size: 16.6 KB (16553 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:9c3a10b3a1822a4b5de7d33abb7528e173bc11f169c3cce9f4e82e8920e48578
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.9 MB (189910643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e7758e4bd9a01efce276b2e39cbef3d9166708b2ac7034d0c7d1fc85ad2e73`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Mon, 10 Nov 2025 04:37:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 10 Nov 2025 04:37:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 10 Nov 2025 04:37:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 04:37:43 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 10 Nov 2025 04:37:43 GMT
WORKDIR /tmp
# Mon, 10 Nov 2025 04:59:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 10 Nov 2025 04:59:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 10 Nov 2025 04:59:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 10 Nov 2025 04:59:39 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 10 Nov 2025 04:59:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65bdf934bab212db989f237b784a2a17e7c8de762196739b48dc1cdde3c370ef`  
		Last Modified: Mon, 10 Nov 2025 04:43:23 GMT  
		Size: 90.8 MB (90752912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75feb09a560d47a7635e68ec0d3466875a2af7812a3f2e0b31e88461f79bdfb2`  
		Last Modified: Mon, 10 Nov 2025 05:03:24 GMT  
		Size: 70.9 MB (70880901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30712a6276ed21055e0e2c2dc8315540f2c575b8f658300be9d5f9a86607d0a4`  
		Last Modified: Mon, 10 Nov 2025 05:03:17 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d268a4c7f16bdf073478c290ade4c20ddc5d351f71283041ad83cbcfae86163f`  
		Last Modified: Mon, 10 Nov 2025 05:03:17 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6c5279f6c4d95db3f880f8c44b528f53dd1d6c17a6666c8780eed34ea6a7890b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5213545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20bf9f793e7d79d5c3ff0d85eca7ce5ab757542d3e621fae8cdf33a37d7bceaa`

```dockerfile
```

-	Layers:
	-	`sha256:c986a33fba6dfe97a9697c6854b7d2b6d28578c8952a07d7d7c9a277cad46e32`  
		Last Modified: Mon, 10 Nov 2025 07:38:10 GMT  
		Size: 5.2 MB (5196992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f419a37463157579915342e7bd0a142796a482b05bbd893cf55890308c96bd6c`  
		Last Modified: Mon, 10 Nov 2025 07:38:10 GMT  
		Size: 16.6 KB (16553 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:b137eb4ea03a0a1ea4a486e3870ed4ad26860b492590c86c5302df6d713441ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.0 MB (191002736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac97fe8e5cc3e82c3107d01a905a36ffcce09967530f37e53fd42a8ef9e0bb12`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 01:05:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 01:05:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 01:05:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 01:05:17 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 01:05:17 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 01:05:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 01:05:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 01:05:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 01:05:33 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 01:05:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6caaf1bf2eaff841716be7f4120bd0c93953d5dead6cd3fa791ee8e3f680ab37`  
		Last Modified: Fri, 14 Nov 2025 01:06:18 GMT  
		Size: 88.2 MB (88210741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18800796e1e1ef1410fc6b628f36caae62d7b481bc990a1a4a38ade6ca029fd9`  
		Last Modified: Fri, 14 Nov 2025 01:06:20 GMT  
		Size: 73.0 MB (72953561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:793a389e5442b617acc4634818b1bbf786c1fc0bd53102fdb13e34b6ae6cc721`  
		Last Modified: Fri, 14 Nov 2025 01:06:06 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72ca4733d36137f1de64a5a7336529b6db75e717b179a80c2d195aca0c516563`  
		Last Modified: Fri, 14 Nov 2025 01:06:07 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3f12f9857389bc89edc32fa3cb06f04fe4b496a8098bbb8d5ddfae17310ce785
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5222483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d77ff8e7f2ef217b58d8d481455b8c3e723d47b5cf864b45f3f5c5394cf6a5f6`

```dockerfile
```

-	Layers:
	-	`sha256:85c3c847b1247cf5f7f0f35855c282427a84f5cd9d6b83cd7086a461d85edf7a`  
		Last Modified: Fri, 14 Nov 2025 01:49:00 GMT  
		Size: 5.2 MB (5205991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3834a94a6edabd079d9e2109df5640d54188735a0fdbfdbe23f9cbc60fe065d8`  
		Last Modified: Fri, 14 Nov 2025 01:49:01 GMT  
		Size: 16.5 KB (16492 bytes)  
		MIME: application/vnd.in-toto+json
