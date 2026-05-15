## `clojure:temurin-21-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:eaf31b0bbe32e7c7584804a38fb2c4c0be07f265d5bc37d1acbd4446891da003
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:9b5b8b91972ef53ce3825eb9671b004b6075f9b3646e0538667360d87cab510c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.6 MB (281555470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d77ddbb01e57190f051677b2f0456c0520237c47881c3bc0e9fc612da19e4e9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Thu, 14 May 2026 23:35:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:35:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:35:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:35:50 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:35:50 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:36:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:36:03 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:36:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:36:04 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:36:04 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1c662d8f6b122c4f09d6ae1b210df55a5ba6e7b529807c0757ccba0c1ac508e0`  
		Last Modified: Fri, 08 May 2026 18:23:06 GMT  
		Size: 53.8 MB (53763343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a6a87ae14dc872e5913137244bc799426bfd88b1fb56d03ddd55fd3677efcb`  
		Last Modified: Thu, 14 May 2026 23:36:26 GMT  
		Size: 158.2 MB (158166940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59eb35090b87fabb440afad1c7e837c18df1a899ee2e5123eb753a61854a2e42`  
		Last Modified: Thu, 14 May 2026 23:36:25 GMT  
		Size: 69.6 MB (69624143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749627bc379228e8d18ba1305da6ef04642888cc28b7fd2ed5f7f130e7c82dc4`  
		Last Modified: Thu, 14 May 2026 23:36:21 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca1a016c0d2479eab9ea269e0ccf95741cff0f1b46d6d332b8ab4263488d590`  
		Last Modified: Thu, 14 May 2026 23:36:21 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:5225c976f7b2bd54a7fb890e420f9dc76fcf20fdad876f476d1323ba14986fcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7426062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:735ae865467c3c48d00f98db23c6ef489536ee4da6d86f299b2de7ca96bafe11`

```dockerfile
```

-	Layers:
	-	`sha256:7bc10d03e3279adccd943c979b7825f5332b83322259f2e174e38578ec0c0c76`  
		Last Modified: Thu, 14 May 2026 23:36:22 GMT  
		Size: 7.4 MB (7410130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d92b8b106c8f6008ec84cef4fc7888c71287d7a4eb7fee85830becd2ffcc2f0`  
		Last Modified: Thu, 14 May 2026 23:36:21 GMT  
		Size: 15.9 KB (15932 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a466a01c0dba240b8e44c87ac5d55c4f3c65aec3a72761f83ba4412dbe777769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.5 MB (278479887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3fd2fb3b17b4bfca328b70ef110df8f729a1225edd71b93d78720e96a8caf0a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Thu, 14 May 2026 23:35:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:35:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:35:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:35:50 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:35:50 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:36:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:36:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:36:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:36:04 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:36:04 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:965b6eb1fb4a74ed46e659c8fd725e1bec9bed6684b59cbca85e48b6c25a32c6`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 52.3 MB (52253210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943c19b4afd70417c9c5ec522c9c9116999a9a62470e556df6f7870613d6ad5d`  
		Last Modified: Thu, 14 May 2026 23:36:28 GMT  
		Size: 156.5 MB (156461249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234adf2b59b7f360f0d05ff4ab456f35734397aa5c92c4bf29cca366cb2e838e`  
		Last Modified: Thu, 14 May 2026 23:36:27 GMT  
		Size: 69.8 MB (69764385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5b46a9da270dbf90a200f36e1039a5b8aadc5a808ed0fb1a5f1fd1a20962c4`  
		Last Modified: Thu, 14 May 2026 23:36:23 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995f1d7d7fdc8476de9e21e6c38ee7a1e0c255b24d93cdb12033263ed8669ebe`  
		Last Modified: Thu, 14 May 2026 23:36:23 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:2776c04b65063cc408d033597455d385261cfa645e04386c12cf0157e993bcf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7431279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce127273d6d60183768f564e6daa6c182c7ec84231e9e0112d636f04cded2fdb`

```dockerfile
```

-	Layers:
	-	`sha256:b9653d8367d1579ac5b8b21e5e8003e0940731929aa8a313e9cf94ea98464cd8`  
		Last Modified: Thu, 14 May 2026 23:36:24 GMT  
		Size: 7.4 MB (7415229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1d24b725e08464540a36010c19e3c8e019deccb1379cfe6e56099154fa138f8`  
		Last Modified: Thu, 14 May 2026 23:36:24 GMT  
		Size: 16.1 KB (16050 bytes)  
		MIME: application/vnd.in-toto+json
