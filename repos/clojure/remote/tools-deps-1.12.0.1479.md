## `clojure:tools-deps-1.12.0.1479`

```console
$ docker pull clojure@sha256:394a28b76433519aebdcf72d9ea53920c8718f3d340c7a2b7e39db4dd72934e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-1.12.0.1479` - linux; amd64

```console
$ docker pull clojure@sha256:179454a5cda366de0d61e098da4e24ed48104d1ccbc12b8730b996074a4c574d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.1 MB (289063500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68520693434aa570ef590d28d3d3540c0542945e9370ce45411debc385c7cca2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae5f884511f0c8616e76244247333cfedb6a1b2470c6df53b011ecd3220e00c`  
		Last Modified: Thu, 17 Oct 2024 01:14:01 GMT  
		Size: 158.6 MB (158579313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e050929c2cd1c7410d434a540b50ebefc08681a2ffe7e9daf2cf8674456458`  
		Last Modified: Thu, 17 Oct 2024 01:13:59 GMT  
		Size: 80.9 MB (80928127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64c17044a2fd1e1fb24339d581c9f523fb8caac886feb1b1c4bfb6b6f54ecd9`  
		Last Modified: Thu, 17 Oct 2024 01:13:57 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0080db915255b3d9754404cfdfff0e82130024744204a61a71c70ff0290d702`  
		Last Modified: Thu, 17 Oct 2024 01:13:57 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.0.1479` - unknown; unknown

```console
$ docker pull clojure@sha256:b10571de1b973d14b8c4c5629362cdb21e2077fba71050888139ade61f8c3a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7179225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cea0b8ace073dbcbd74a71f5bd28aeac60bcc8ee649aedc931fec07ae03f87f1`

```dockerfile
```

-	Layers:
	-	`sha256:334e43b44903feaa500e24d566ef4f096f6adcb518b3cddc685b6ed0ab8c9311`  
		Last Modified: Thu, 17 Oct 2024 01:13:57 GMT  
		Size: 7.2 MB (7161747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2b4f20ef4e00a0a2ebe42329b61e59439b1de46278e1cc4f0d78451e798646e`  
		Last Modified: Thu, 17 Oct 2024 01:13:57 GMT  
		Size: 17.5 KB (17478 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.0.1479` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1e27816a80cee76298bb9a20404a6e84c704845fd425fdb32e28159190ea8c60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.1 MB (287122266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e7ac5011b906f19dffb482cd5e6d9c34598d54142c955cc0b42556aa9ec13e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6081bef755cabe28916d335d34f5e5bff03f6905db8f85e9e22d2927f98411a9`  
		Last Modified: Thu, 17 Oct 2024 07:54:30 GMT  
		Size: 156.7 MB (156746192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e21c332a61721f87a6ce622518a613e108366928b4035a527c56b208c9deb74`  
		Last Modified: Thu, 17 Oct 2024 08:23:01 GMT  
		Size: 80.8 MB (80790054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23d5f751a68fb74937aa3119c1af668be06b9617c105674a47cd29ca20e2a0f`  
		Last Modified: Thu, 17 Oct 2024 08:22:58 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a7b4c59a9ff684bc17cd35bc69a34b1a24a94cb1b5876caaa02816677dd2446`  
		Last Modified: Thu, 17 Oct 2024 08:22:58 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.0.1479` - unknown; unknown

```console
$ docker pull clojure@sha256:c3013576dde8bb5b2dbf531e1007965628a2512cce641532cc7458b8c9dc0299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7185243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cedd10b9bd72ba2dbe804298112f5790ce90c62764084a7fefea1b39ea41e5c1`

```dockerfile
```

-	Layers:
	-	`sha256:3dab7c8d34dbd5f1ebad5ad50e1645901ddf0246fb03423ce09ef08e8a011ba1`  
		Last Modified: Thu, 17 Oct 2024 08:22:59 GMT  
		Size: 7.2 MB (7167587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcfdbc6c65b750289a607a77b84e0d6602d949ef9587feda44b7f292e93b71b1`  
		Last Modified: Thu, 17 Oct 2024 08:22:58 GMT  
		Size: 17.7 KB (17656 bytes)  
		MIME: application/vnd.in-toto+json
