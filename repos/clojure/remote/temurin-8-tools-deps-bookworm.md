## `clojure:temurin-8-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:3ffac339ce2abf442d5f7f76ad95259bfd86cd2248c814087742b3fe3e22a8e3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:d0536cda3d420cf97026c4a4b8e48a00433e9fce3b7fa3bc1b05759b2879f8c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.8 MB (184809947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87e51e8a4975faf18bfc0cb236bfd6964be7ecbd9c05deabdf7504e5580cbe6d`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:52:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:52:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:52:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:52:04 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 19:52:04 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:52:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 19:52:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 19:52:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e226332ea3f9c564edeb3bbde63b3c9d476d133dc336dbb442852ec2fdae2ddb`  
		Last Modified: Tue, 24 Feb 2026 19:52:33 GMT  
		Size: 55.2 MB (55170133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:275a0569b6f64e6bedb508c276ce3681c8c38021d4fa2233f9d6a876d02200c1`  
		Last Modified: Tue, 24 Feb 2026 19:53:12 GMT  
		Size: 81.2 MB (81150392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44b07c331bd616681705cfa2a36f5c5978a1027e667fef4fb633b747d768bf1`  
		Last Modified: Tue, 24 Feb 2026 19:53:10 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:0f01aa7b61a264831d0a283e7c02a54b92ed71511207f5aa9bbf8881e081e724
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7511169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a0a9018ce976443771251af5532fe7c86e35d2c53561e285063d7d1cc659558`

```dockerfile
```

-	Layers:
	-	`sha256:d7d1a3515a92567ba0cecc7dd0a5cde9863f86bbc70514889dbc5abcc023662c`  
		Last Modified: Tue, 24 Feb 2026 19:53:10 GMT  
		Size: 7.5 MB (7497776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d05182cfa98818233f4b0fc6efc8f8e88c9793bca71baae931b3b55580413b0c`  
		Last Modified: Tue, 24 Feb 2026 19:53:09 GMT  
		Size: 13.4 KB (13393 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4b99fcbb86387250a5480ed866484824f88a8e0f7da0fe4d0ea621432cfde156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.8 MB (183763394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a3943eee9074a8fbda44b6c3b70c7bd5cdab7e7e49ba89edc3e7b44b809b86`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:02:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:02:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:02:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:02:36 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 20:02:36 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:03:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 20:03:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 20:03:28 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5899fd4281eb802180094cd7248a180de2d7f4dd4fadc1ad27cbfc97e09414b`  
		Last Modified: Tue, 24 Feb 2026 20:03:03 GMT  
		Size: 54.3 MB (54251619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c86b412715f7bd495609651ebb01774213c75407fe03c8f99f0a85c19449b4e`  
		Last Modified: Tue, 24 Feb 2026 20:03:46 GMT  
		Size: 81.1 MB (81137919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9fdda5e6f9f18e0bf0054750bd5cae51aaf0424b484880511f52385ab0e8b3`  
		Last Modified: Tue, 24 Feb 2026 20:03:44 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:5d2d3edb51c40ae64a50bdc9fe29a536ae4b10107f671114f5a257a01387e9fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7517749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77faffb1c0aa1262d65df22344467af2ad1cfe94d6aba67b2ab81b04b361c8a8`

```dockerfile
```

-	Layers:
	-	`sha256:9f4e21ce246a3251150dd7502b0f2ddf4b2b386a7fea76223c50fdca48955f4a`  
		Last Modified: Tue, 24 Feb 2026 20:03:45 GMT  
		Size: 7.5 MB (7504239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d13df1ad3d2838f558b4b5d120ec607cb5eaa633d0237c1f9d688e50a2564a9`  
		Last Modified: Tue, 24 Feb 2026 20:03:44 GMT  
		Size: 13.5 KB (13510 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:cc448b5b7ae08a7c9ee434390ea8e60430a358b8d8c6c7b617d35cb149845f55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (191965445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec9c9a187d1c84db1f0ff09d3123c270e610e6c14a30555ca227e6b405a0161`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Thu, 05 Feb 2026 23:55:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:55:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:55:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:55:41 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:55:43 GMT
WORKDIR /tmp
# Fri, 06 Feb 2026 00:03:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Feb 2026 00:03:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Feb 2026 00:03:13 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:5e189aacb842725e8d1d9877c9ab9af09e14901412b6665e179393112b5bca51`  
		Last Modified: Tue, 03 Feb 2026 01:12:57 GMT  
		Size: 52.3 MB (52327289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:081c85e0b853be6e0d03b2fbec5e5c7dc3f5e5b6e6f27d9574958d9f52776d65`  
		Last Modified: Thu, 05 Feb 2026 23:56:59 GMT  
		Size: 52.7 MB (52650375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a2f301a831dc7cbc558f088450c2cf45b3c5f2e488ee9f6ea35709dcf89fd6`  
		Last Modified: Fri, 06 Feb 2026 00:04:05 GMT  
		Size: 87.0 MB (86987133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d705504f3e16763e7ae933471916cd0d41c2e47031f616a694a9732a7532cde`  
		Last Modified: Fri, 06 Feb 2026 00:04:03 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:8ee5adc593ca61f27cc65fbf54f3e84f785f8a0460588e9cf841ab0325621703
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7517829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e742db29026c15eb6b10477789b0945c4464380ae8f8c122af6865f977e1371`

```dockerfile
```

-	Layers:
	-	`sha256:23351281fe5467a4c7e9ed741d0a807f680df4994edcf0fa41938c90ccbb2bfa`  
		Last Modified: Tue, 17 Feb 2026 23:29:52 GMT  
		Size: 7.5 MB (7503587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:babe5b75f5005839c7db58619362e2759a30a49a9fed40168be170925c7c0024`  
		Last Modified: Tue, 17 Feb 2026 23:29:52 GMT  
		Size: 14.2 KB (14242 bytes)  
		MIME: application/vnd.in-toto+json
