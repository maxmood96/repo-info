## `clojure:temurin-17-tools-deps-1.12.4.1602-bookworm`

```console
$ docker pull clojure@sha256:271b51a8b629043a3a308c50e04f0a957ae7410a15a1fae461b33465da6579b2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.4.1602-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:c58d6136cdec7d53a85ae6c98eae143348d8e97831c5787d0259bb735008f598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275261607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca23abcf8274e8a0661a570db162ab664fffbae3dee2b91f61f60d81e7a33b0e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 21:43:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:43:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:43:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:43:01 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:43:01 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:43:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:43:15 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:43:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:43:15 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:43:15 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af31c8caebeea238348885601aa5053fc3f48d92dfe059a29b47d296f7fc3cb5`  
		Last Modified: Tue, 17 Feb 2026 21:43:39 GMT  
		Size: 145.6 MB (145628776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba23b01869ed80663ef582edc38d3c9b1f293c6c2bb78f4d63e24f5b03d5ddfe`  
		Last Modified: Tue, 17 Feb 2026 21:43:37 GMT  
		Size: 81.2 MB (81150305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e89dd1e582744b333242cf98eab92fa975268007e96f01f0ace851a842bac5c`  
		Last Modified: Tue, 17 Feb 2026 21:43:34 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b26fb32d51f9e45100d8f2d0a65295156640df59ccee4ad0b76333cc410ad6`  
		Last Modified: Tue, 17 Feb 2026 21:43:34 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1602-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:acdae60ab88a8557ff7e595fa10d2a6de3323b185477c6914ff872bad8f4baac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7392567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e1c8f57936820622658c141c165f9e77863019711c4763104d1737a39c3016`

```dockerfile
```

-	Layers:
	-	`sha256:0e8aa88ac97bef0cfaee541569c62d100fc13780d028c8cdb15db60c66ab7f63`  
		Last Modified: Tue, 17 Feb 2026 21:43:35 GMT  
		Size: 7.4 MB (7376789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a43a321f6bf8876ac261b3e641e2b30852c173ce38b2673562b70dfe0c48ee8`  
		Last Modified: Tue, 17 Feb 2026 21:43:34 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1602-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:51ae1678b90ff14c79b73f3d1768adaf04ad8842e305c3980f0e782164bdccd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.9 MB (273941691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1afcc11e20bf17f31019f86ed5cad20edd2976a7ae3b189c9485d828edad5b02`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 21:42:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:42:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:42:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:42:59 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:42:59 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:43:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:43:14 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:43:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:43:14 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:43:14 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:64e8f4c09e7ac936ecc3deb0e61613f653224c28b2e35fa9d8e6e11cbdb5f911`  
		Last Modified: Tue, 03 Feb 2026 01:13:22 GMT  
		Size: 48.4 MB (48365956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad82f46cbf8c39e3516d05ec6a981004fddc1f7a5989a11aec4daac7bfe2141`  
		Last Modified: Tue, 17 Feb 2026 21:43:34 GMT  
		Size: 144.4 MB (144436241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f42360e4b1d9f932cdee013ee841779a37ecf06e37b776c44b2a2535662161`  
		Last Modified: Tue, 17 Feb 2026 21:43:37 GMT  
		Size: 81.1 MB (81138451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad514758310ead2f90f5d7b6c91d15434ef6f129249ee5af0ebf37dfb87f45ac`  
		Last Modified: Tue, 17 Feb 2026 21:43:34 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4eb3e3bc40005bd50b1271e73403238aed5437a35b7e75c560d2d20e410c74a`  
		Last Modified: Tue, 17 Feb 2026 21:43:34 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1602-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:573a8e67990c090e1f2029c012e79980c8b8b8c5e58b4d3aca5bd5412c40f4b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7398448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3b5c6905cfac9727a9bf146644e9a7c19704c978c88eacacff9c5d158855920`

```dockerfile
```

-	Layers:
	-	`sha256:6e7b0ae41cd089eddac377c999ab4832075aa2a2fc4c4fb0035c86c09e411219`  
		Last Modified: Tue, 17 Feb 2026 21:43:34 GMT  
		Size: 7.4 MB (7382552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aca562276897b5ffeb9761cc9cf198a6820d10dc09a563078c596fe906361721`  
		Last Modified: Tue, 17 Feb 2026 21:43:34 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1602-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:f012e31ae716a00efdc0f4140d08ce963ae3bc548792140293d357399f368ba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.8 MB (284753733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ee2d01ef483a466e9fce74ae23c0249e7d225d3374e3b6395a937c57d548cd8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 23:45:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 23:45:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 23:45:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 23:45:07 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 23:45:08 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 23:51:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 23:51:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 23:51:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 23:51:43 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 23:51:43 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5e189aacb842725e8d1d9877c9ab9af09e14901412b6665e179393112b5bca51`  
		Last Modified: Tue, 03 Feb 2026 01:12:57 GMT  
		Size: 52.3 MB (52327289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2bcebe1436b2e06a46e1026a9f267beb7b738921e7b714b94ecc1b9526b812`  
		Last Modified: Tue, 17 Feb 2026 23:46:43 GMT  
		Size: 145.4 MB (145438175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2ec25b5b4b77d0be2c0e13d34b98eeca85dea2f994c87a633eda9c91ae2e05`  
		Last Modified: Tue, 17 Feb 2026 23:52:26 GMT  
		Size: 87.0 MB (86987224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40eccf9a120a020ec35bfa7bd8b45f4a102b2229ecfc9ad328742f1905cbc8db`  
		Last Modified: Tue, 17 Feb 2026 23:52:23 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3968773ccb607047341bae3f5f302d28880d52bf8df3af77b3a969391d7344`  
		Last Modified: Tue, 17 Feb 2026 23:52:23 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1602-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:bab88806d93f88a22d5e59c0aef79dc71eff2b0ebc99968226fd8c650f2eac9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7397831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5e02cc67357d086bfd2859b155e862d3be4924787679b1cbed87e6764bff676`

```dockerfile
```

-	Layers:
	-	`sha256:415a15517a3708c3d1538b4295fe034f67914f146fdd86c8cf63303f23f43e50`  
		Last Modified: Tue, 17 Feb 2026 23:52:24 GMT  
		Size: 7.4 MB (7382005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5355b65ae0cc9dd3a3951fce0e824393d35c5feb10763727d022ed6f7951660d`  
		Last Modified: Tue, 17 Feb 2026 23:52:23 GMT  
		Size: 15.8 KB (15826 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1602-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:f0d9d0eba696eeff4e39cd5a140ff37d3b6867c058c2587530f7fd3acdcd6c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.7 MB (262730139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42b5f9427977557b57eb438de56b7962f4b5d2e286b97c6a429a172fe7abca59`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 22:08:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 22:08:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 22:08:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 22:08:02 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 22:08:02 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 22:08:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 22:08:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 22:08:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 22:08:44 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 22:08:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4c4c4621da5085342b3b0d8d8ef57e5e44004eedf5818268af30c41a02cb6cf2`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 47.1 MB (47138343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51e535dc0d305223a844c3403214deb9ebadafbe1230d72a59516621edab4af`  
		Last Modified: Tue, 17 Feb 2026 22:09:23 GMT  
		Size: 135.6 MB (135627120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fac0f3438fb97703862fe1a360c7b738eb90b53b6e51b06e0b2272d9fbb62b`  
		Last Modified: Tue, 17 Feb 2026 22:09:26 GMT  
		Size: 80.0 MB (79963630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8114ff17ded5acf65b5581f501b987e1b76658799eb9188554c74eeb998ef5c`  
		Last Modified: Tue, 17 Feb 2026 22:09:23 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79abe58c641c1e3a0f2c104e5649d172ff01c9c0f6d1279e1919793db821c56a`  
		Last Modified: Tue, 17 Feb 2026 22:09:23 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1602-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:fd4e247b80f8fb28c4e27017ed3d7d3dba08dcd2af185b4191bd8545f091a132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7383886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b28f6c85533d5fa0d9e6ad980be9d2f7e578b608784c7da77c012b980bf3695a`

```dockerfile
```

-	Layers:
	-	`sha256:b644b3b80d5f0bef719e809e570ca8f4f4f5b3337ab06bdef33569111b7146d0`  
		Last Modified: Tue, 17 Feb 2026 22:09:24 GMT  
		Size: 7.4 MB (7368108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9838ed0d57a15449de1a5e7917a5ed736b6303ed966955ad2a742b0a5d62d43`  
		Last Modified: Tue, 17 Feb 2026 22:09:23 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json
