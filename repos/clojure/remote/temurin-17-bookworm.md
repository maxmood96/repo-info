## `clojure:temurin-17-bookworm`

```console
$ docker pull clojure@sha256:b50aac467b1e2c3aea9a5c8d0c0b07a7726f06c691a0159b73e65fbbe58c0e1f
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

### `clojure:temurin-17-bookworm` - linux; amd64

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

### `clojure:temurin-17-bookworm` - unknown; unknown

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

### `clojure:temurin-17-bookworm` - linux; arm64 variant v8

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

### `clojure:temurin-17-bookworm` - unknown; unknown

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

### `clojure:temurin-17-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:eec4f790d694d9df386c7a4cf4ec9c60eaff76c8a64fc2e71e06e3f2de3d0bc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.8 MB (284754058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94cd35fe249316ba73cac4ff85f97399b072f93e55194060cd8cb078bed0b8fa`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Fri, 06 Feb 2026 00:22:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Feb 2026 00:22:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Feb 2026 00:22:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Feb 2026 00:22:02 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Fri, 06 Feb 2026 00:22:04 GMT
WORKDIR /tmp
# Fri, 06 Feb 2026 00:29:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Feb 2026 00:29:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Feb 2026 00:29:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Feb 2026 00:29:08 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Feb 2026 00:29:08 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5e189aacb842725e8d1d9877c9ab9af09e14901412b6665e179393112b5bca51`  
		Last Modified: Tue, 03 Feb 2026 01:12:57 GMT  
		Size: 52.3 MB (52327289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56445963f10f9073db32d8e55af4130cabe6e777336d5f50276061d989325f1a`  
		Last Modified: Fri, 06 Feb 2026 00:23:46 GMT  
		Size: 145.4 MB (145438231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29be333cc538a2f3c47605f69d23f52f8be2c437f219bf3a21ad6e020d638791`  
		Last Modified: Fri, 06 Feb 2026 00:29:52 GMT  
		Size: 87.0 MB (86987495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656446c9afff452c9b55638a0f6c5745de12a623f61b71993fee0b64ba5d1bbe`  
		Last Modified: Fri, 06 Feb 2026 00:29:50 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc632d7cce830c7507a4215eb08387f64507c26c6565b1dcac130f796a71085`  
		Last Modified: Fri, 06 Feb 2026 00:29:50 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:84db571d86f61421ad9e95ec41a3791a7c8019aa6a6f43efc2a46d6d10ab7fb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7397831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:468398dfa10eb8de2a3de58cf344ab5c4c3b28035ce783f6457f710011c5a580`

```dockerfile
```

-	Layers:
	-	`sha256:f2889273650b55b195003afdd579628d5393fb36dbcd2bb9c05f49320cc67678`  
		Last Modified: Fri, 06 Feb 2026 00:29:50 GMT  
		Size: 7.4 MB (7382005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44114b927ae4a9f8e6c6029a3ace8420d5994cd908a28bd8c49d6527a8b718ac`  
		Last Modified: Fri, 06 Feb 2026 00:29:49 GMT  
		Size: 15.8 KB (15826 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:a553f96e0762fba7d339d7bee2f0aceb4e46a254d4cf9b65d36f125c9cb16a0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.7 MB (262729458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad70e9c67897912950b74af24b60a7b08a09f9c5bc6392697bb73eb07a14595`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Thu, 05 Feb 2026 23:03:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:03:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:03:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:03:40 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:03:40 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:03:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:03:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:03:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:03:54 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:03:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4c4c4621da5085342b3b0d8d8ef57e5e44004eedf5818268af30c41a02cb6cf2`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 47.1 MB (47138343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dbe423369c66772a10b6323256e13377c198dc15418b011949a2282709c4a89`  
		Last Modified: Thu, 05 Feb 2026 23:04:27 GMT  
		Size: 135.6 MB (135627054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebceae15a4733d13c4dbc4081dcc159bdcb824dd35cb1505563cad5fcb1fde1`  
		Last Modified: Thu, 05 Feb 2026 23:04:26 GMT  
		Size: 80.0 MB (79963019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e39674d93bb3bf171767057d80ee7b33c86fd5ef9615898c2c0eb0b8ba1cd0d`  
		Last Modified: Thu, 05 Feb 2026 23:04:23 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35092513dc0334dd3b2322c722ca158cb4c3200b24ac2836335b4bedc0847f19`  
		Last Modified: Thu, 05 Feb 2026 23:04:23 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:ef602f52f49d6400e42be4f30c7f5d3def4a1012a11931055a1e9f5baf504529
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7383886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a83c15a8979690e96041c7a75a3cb85a27e3df0040f84f0064467ff2af860158`

```dockerfile
```

-	Layers:
	-	`sha256:d8f880b9142e62c9560df7802f62c90f1b2f498f3fdfc6db511face8df1a1235`  
		Last Modified: Thu, 05 Feb 2026 23:04:24 GMT  
		Size: 7.4 MB (7368108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eea94729678f7d659203bb9d599411459cd46f0dcbcddd94409e126dc7ba1c53`  
		Last Modified: Thu, 05 Feb 2026 23:04:23 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json
