## `clojure:temurin-17-bookworm`

```console
$ docker pull clojure@sha256:fb7ed9997ea42e90b9f414b7fa2adb5cd7bdb55e9133a897ce4065bc8726ffa2
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
$ docker pull clojure@sha256:8a3a60856d6da7eefc2069a0533141456be5c7a06a28ef47981d15b52a6da347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275261378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb70aac82e2b014800f883459ea17f9b44ccafa46c934c83005a65d1404d2ed4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Thu, 05 Feb 2026 23:04:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:04:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:04:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:04:36 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:04:36 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:04:51 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:04:51 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:04:51 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:04:51 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:04:51 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a949f27bfa776da98d0e2e8b6d50b054fa5b6227cb279befa4db7addd705f51d`  
		Last Modified: Thu, 05 Feb 2026 23:05:15 GMT  
		Size: 145.6 MB (145628494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13865ab6426ac31fd802859502011737fa44abeb9a5ebceb8d5be337c0c7edfe`  
		Last Modified: Thu, 05 Feb 2026 23:05:13 GMT  
		Size: 81.2 MB (81150357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffcadfddb560fd9642b4b1f50bf8f691838374b9750fa119ddc8b76454e2e559`  
		Last Modified: Thu, 05 Feb 2026 23:05:10 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58f447578d51771126529db4976cbaaeff3b74164130fae54df2f14177c4ff6`  
		Last Modified: Thu, 05 Feb 2026 23:05:10 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c10878c8cb7a05d0cc31e7c84d70102c90b70149e210238c3b8a3ac8e0f26e32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7392567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4c058d6e0142e59267599413ce34e1754849a2aa1a64bea863b8aacd451a252`

```dockerfile
```

-	Layers:
	-	`sha256:3d8c86f0dc5ae173831060d47c09443ac5b843c1b410c4b59dea01ae6843bf22`  
		Last Modified: Thu, 05 Feb 2026 23:05:11 GMT  
		Size: 7.4 MB (7376789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2dd997c9d7e9de1fe5fb3c96d91d9a749898f829536dcac9871c268a6362d58`  
		Last Modified: Thu, 05 Feb 2026 23:05:10 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9e7531d3aa8c22747cc78948d5677415e9cde01d1913296ee017aa9f73b0653c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.9 MB (273941586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39762155acbd488a5c2ff7ed24490337bf2ca673c3ba41d38902b3e265097487`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Thu, 05 Feb 2026 23:05:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:05:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:05:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:05:28 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:05:28 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:05:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:05:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:05:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:05:44 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:05:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:64e8f4c09e7ac936ecc3deb0e61613f653224c28b2e35fa9d8e6e11cbdb5f911`  
		Last Modified: Tue, 03 Feb 2026 01:13:22 GMT  
		Size: 48.4 MB (48365956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4a7e6e074fbdd49be5557e90960fd600d25d749f4efc95cbf51ef3d089258c`  
		Last Modified: Thu, 05 Feb 2026 23:06:07 GMT  
		Size: 144.4 MB (144436240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca35df327527ccd5975969e562c016a177003c1e25683031766c4702f7e591c5`  
		Last Modified: Thu, 05 Feb 2026 23:06:06 GMT  
		Size: 81.1 MB (81138346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0458e9cf38987bae48dac216a026f545958cda9bfbdc40ef864b4de35f5093e2`  
		Last Modified: Thu, 05 Feb 2026 23:06:03 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46dd71bf1bfe4831f97945dafab47acf9c7f2981f0047aa8de848ead39c3c98f`  
		Last Modified: Thu, 05 Feb 2026 23:06:03 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:7b7baa98b4792e71a6d73e085fe9d56b636bc442778dbb0d542eab1b7ad7228e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7398447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8b9418366f9105af61059538d6825195fd7fb5b11c7bfd1c9c92ab5950194fd`

```dockerfile
```

-	Layers:
	-	`sha256:29bfa43f4d48c15cde3231e21c42ea861f783ae4f757c899d3eb77cd7e4218c6`  
		Last Modified: Thu, 05 Feb 2026 23:06:03 GMT  
		Size: 7.4 MB (7382552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdfab601e8a6c17fde870e7b5216c1989c6d9b6c6a551679fcfb97b38f8549ed`  
		Last Modified: Thu, 05 Feb 2026 23:06:03 GMT  
		Size: 15.9 KB (15895 bytes)  
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
