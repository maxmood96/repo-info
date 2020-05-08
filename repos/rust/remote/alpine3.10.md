## `rust:alpine3.10`

```console
$ docker pull rust@sha256:2c9578a18535088e2657a972c8a46d52740ef06053c65f2e23ac880dc947b872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rust:alpine3.10` - linux; amd64

```console
$ docker pull rust@sha256:2138926247bcb0218954bd17643859931454ecf6ea4ccf66cb1a0f27b518820b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.2 MB (135182146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0da36b2e9e20cdd07f2f2c1f37e0b4e0dfe4ac8638bbb880976a14373cbc15b0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:21 GMT
ADD file:66a440394c2442570f1f060e25c86613cb2d88a8af0c71c5a4154b3570e9a805 in / 
# Fri, 24 Apr 2020 01:05:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 12:43:33 GMT
RUN apk add --no-cache         ca-certificates         gcc
# Fri, 08 May 2020 00:21:54 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.43.1
# Fri, 08 May 2020 00:22:06 GMT
RUN set -eux;     url="https://static.rust-lang.org/rustup/archive/1.21.1/x86_64-unknown-linux-musl/rustup-init";     wget "$url";     echo "0c86d467982bdf5c4b8d844bf8c3f7fc602cc4ac30b29262b8941d6d8b363d7e *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION;     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:21c83c5242199776c232920ddb58cfa2a46b17e42ed831ca9001c8dbc532d22d`  
		Last Modified: Fri, 24 Apr 2020 01:06:07 GMT  
		Size: 2.8 MB (2795580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c357195eea76782bc410a7e9f62d18d5ed63a9bd29c0e4b6807159490aa1ab`  
		Last Modified: Fri, 24 Apr 2020 12:44:44 GMT  
		Size: 34.0 MB (33982304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff59da6a88f8c42beb024bbe27f7d4750b2280cab046f41469e6534ff3f2d825`  
		Last Modified: Fri, 08 May 2020 00:25:08 GMT  
		Size: 98.4 MB (98404262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
