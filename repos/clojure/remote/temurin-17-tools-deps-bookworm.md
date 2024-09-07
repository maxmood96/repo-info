## `clojure:temurin-17-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:88e37fdaebfece6dfce291c16dabd5dab60a627d49322ac0bd2b343efe1a57a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:f93971cc87d08b63ec3587dff1817080e5f6643f71d3e08c18fc3e4093f1a25d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275422828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06905accab2bc169a2e9aaa28bf0ac34f63cd4885f7a32a22777f35518641fc8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:36 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
# Wed, 04 Sep 2024 22:30:36 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a74cfecc2d0c6de56ffa9b246a6b10045d14c1d47e8090b0ef302345139b0193`  
		Last Modified: Fri, 06 Sep 2024 20:58:23 GMT  
		Size: 145.2 MB (145166507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e27d18a65f3c5da0f1bdb4d658fa48eb55d1a8d027ebc833c339da33b5e723`  
		Last Modified: Fri, 06 Sep 2024 20:58:49 GMT  
		Size: 80.7 MB (80698576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba37d581ef67e1f2fb05564e757aa1e7a9ef789131b68a25170cf7f155e6122`  
		Last Modified: Fri, 06 Sep 2024 20:58:47 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcaf0d1747c6a59bbe7d617b2613f0f031dd5cff05ff03c9263bd601e582047c`  
		Last Modified: Fri, 06 Sep 2024 20:58:47 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d6d601f21e78c57045bd0e5ed0c0da2cd15aafba24697da32f4906e33ec96291
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7014911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58cae7732e0262b683aa22019eba002ebd49a4366b788dc7c51a2df24cbd6212`

```dockerfile
```

-	Layers:
	-	`sha256:454a8dfc8948d3a63558629d30e7c4e49107537a389c0866c2d9c71cf49d459b`  
		Last Modified: Fri, 06 Sep 2024 20:58:47 GMT  
		Size: 7.0 MB (6999471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0d7cea234ad057782e380bf8b31307821edd9e551a433201afd35b4c1a2b3f3`  
		Last Modified: Fri, 06 Sep 2024 20:58:47 GMT  
		Size: 15.4 KB (15440 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d24cb91982c6d7ba9de5019cbb1d2aa7778b8f86d9bf6fe92d63b159e434c19e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.0 MB (273993566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a67f83acda517b6e14d6f8225b4fa13844ac546bf0106eebf735c897e9d8c687`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:42 GMT
ADD file:7f28c8fde9feb67359cbf19f7d77d3f757490b5f586520257cf92d233b4bfaa4 in / 
# Wed, 04 Sep 2024 21:39:43 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:56c9b9253ff98351db158cb6789848656b8d54f411c0037347bf2358efb18f39`  
		Last Modified: Wed, 04 Sep 2024 21:42:16 GMT  
		Size: 49.6 MB (49585623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4739aeebae48263039d4595d4e6ce54767ccaea2417dbd8daedf234bb19c713b`  
		Last Modified: Fri, 06 Sep 2024 21:19:53 GMT  
		Size: 144.0 MB (143959441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272ddd5bf7e056f82bcdb6f0c8d312b914a1721dd8ba4be8bc920f7961cc48d0`  
		Last Modified: Fri, 06 Sep 2024 21:25:54 GMT  
		Size: 80.4 MB (80447462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356456cb67b13885a66d588f4cfc698c314ff8953a1b26656b1df276d0ea7a41`  
		Last Modified: Fri, 06 Sep 2024 21:25:52 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0470412c98c29deaf4a3c516e428aea8f0d74579191fd3292f35a5df7dd8c4ed`  
		Last Modified: Fri, 06 Sep 2024 21:25:52 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:59dfa3af4d2f51970992d8506ccf11747acf6fa1de3777dd00fd88e865b21c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7021833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2a2f6e2a4ce572ff966f68f4a44ebaddb9bfc4d920f30b6a2685e2cea2fd3af`

```dockerfile
```

-	Layers:
	-	`sha256:2965afa56231ddbc895f4dbe1c7ec4ef51318b986963cf32e02d86fcedd851c1`  
		Last Modified: Fri, 06 Sep 2024 21:25:53 GMT  
		Size: 7.0 MB (7005858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfebca1c13ba0ae4273bfcdcb4f491f4f54437c9c74bcf9ec012f10ea8f14a09`  
		Last Modified: Fri, 06 Sep 2024 21:25:52 GMT  
		Size: 16.0 KB (15975 bytes)  
		MIME: application/vnd.in-toto+json
