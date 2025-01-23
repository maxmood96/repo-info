## `clojure:temurin-17-bullseye-slim`

```console
$ docker pull clojure@sha256:e817c2d302ec897607e0999de9e2f0dfce8129d9083b8495927322e48fe6f07d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a45ec85345e67da5a05055e7bcd3ad6ee55260e0b31a17922eb9f9e760843194
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233571349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fcecd464796e6ebf356f6d12992a8fc366e6a86144069c01ee091a4ae0a2408`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35538d02efea9e1c6b5b17c32d20f295a37d6c03dd32e488396ee183869125f`  
		Last Modified: Wed, 22 Jan 2025 19:36:50 GMT  
		Size: 144.5 MB (144536751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad873912bdeccced1b8612966e0f9a4076501e2a14095ed0d4eed38680a9fac`  
		Last Modified: Wed, 22 Jan 2025 19:36:47 GMT  
		Size: 58.8 MB (58780896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e81c81720cab6eaf10ad236ec130d962c31721b3a3ff742b18b3b9cda55e1c3`  
		Last Modified: Wed, 22 Jan 2025 19:36:45 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c18f001812438095e01c163f678c1d5a74d9e02ad7a3570f5a9fc690dd7537f`  
		Last Modified: Wed, 22 Jan 2025 19:36:45 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f72159cba3b36c2021e6ff4651ac85e53cf1f424bc1e979bfcdb0ff6a41e1fcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5132948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83f53b34bf53e1942f61906dfcf2e9b97d7de9d840dcd8c745a1e37d0f935ab4`

```dockerfile
```

-	Layers:
	-	`sha256:248aacf2eaac4d4f34569535a195a73915c17a02276a8fe743099c28d04cb717`  
		Last Modified: Wed, 22 Jan 2025 19:36:46 GMT  
		Size: 5.1 MB (5117069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e98b5d0b4e02bda06ff1b7cbaff738b2462c1a3927fc1590a7d435a54841813d`  
		Last Modified: Wed, 22 Jan 2025 19:36:45 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:559efe3b2d2deaa841b8025a66fa94001e739d63565348dda2140689ae3dddd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (231012007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d5ac38c72b863d9069e7cf5ac0a790803820d6271f297a8cdd650e06f1be53b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8046fc472af52cbd0c18bb2ee9a2dba25212fe858739c56750d18c3352f2396f`  
		Last Modified: Thu, 23 Jan 2025 00:48:42 GMT  
		Size: 143.4 MB (143360974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82706dc180b428b48d7c58d6c29a77cbb3b3c01a3dce2d267254e40bc1d959c6`  
		Last Modified: Thu, 23 Jan 2025 02:51:39 GMT  
		Size: 58.9 MB (58905078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a17e3b734470540434d42ffdbcc8a7c68ea2717ac1a6a20711930aa4cfc409`  
		Last Modified: Thu, 23 Jan 2025 02:51:36 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bab6d847a09b81de30a407951b931d5b3d3e99f6d018cd0d1ff84f5c8c62d51`  
		Last Modified: Thu, 23 Jan 2025 02:51:36 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4bd04aae96f4d33577cfe7b0aa8bbf98eaa98995ed903d8c6a794bd1c4f10e6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5138798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:086f58c224cb1ead56a26d60dbe5e84d6555d060d1931712c023955c8a17c993`

```dockerfile
```

-	Layers:
	-	`sha256:0ea766beb3caa313efd3a9404b063d557a932500a49f7493c0e6fc607a2a0097`  
		Last Modified: Thu, 23 Jan 2025 02:51:37 GMT  
		Size: 5.1 MB (5122801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e56fa701efa36ac022cdac7f24681ab52a9ba89d00ae132c899a9e25ab8a03a`  
		Last Modified: Thu, 23 Jan 2025 02:51:36 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json
