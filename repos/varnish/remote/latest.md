## `varnish:latest`

```console
$ docker pull varnish@sha256:2af8792bddd0417e8d2d0c8e0786b4c0e9be065b80ee115f0bf25114074579e7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:latest` - linux; amd64

```console
$ docker pull varnish@sha256:8bfe67bb6ba71362e1b442565e7f912093a60a8afdb234a1cf0c00141c070a13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122300682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1acdb5723a581da92b80d250427cc8a460296f65c6bfe64e6da7f663551c48de`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:19:16 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 19 May 2026 23:19:16 GMT
ARG VARNISH_VERSION_NUMBER=9.0.3-1
# Tue, 19 May 2026 23:19:16 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 19 May 2026 23:19:16 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Tue, 19 May 2026 23:19:16 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 May 2026 23:19:16 GMT
ENV VSM_NOPID=1
# Tue, 19 May 2026 23:19:16 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.3-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 19 May 2026 23:19:16 GMT
WORKDIR /etc/varnish
# Tue, 19 May 2026 23:19:16 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:19:16 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 19 May 2026 23:19:16 GMT
COPY index.html /var/www/html/ # buildkit
# Tue, 19 May 2026 23:19:16 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 May 2026 23:19:16 GMT
USER varnish
# Tue, 19 May 2026 23:19:16 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 19 May 2026 23:19:16 GMT
CMD []
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e26b5e52e0be220474779970dfdf187aae680692689dea55794041db044bade`  
		Last Modified: Tue, 19 May 2026 23:19:31 GMT  
		Size: 92.5 MB (92517867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b05db55626b2451dbace6b4288830c9b440be1ecfdf4ebcb6a5b452b92d578fa`  
		Last Modified: Tue, 19 May 2026 23:19:28 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c30bab11eda8acb4bdb67b0e9fdcdb25881a9aa085b82541741b11d6c39941`  
		Last Modified: Tue, 19 May 2026 23:19:28 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e3f3ea658509ec155a6f9b75f068c244ba52dfd18648ee5e6a677791b9094d`  
		Last Modified: Tue, 19 May 2026 23:19:28 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:8585b078104c58c7bbd43d65b105f7d4e0a8b0fdddfed297c78a0e9958bc0add
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ee409ab6cf8e60eef05e6c4c7fca813c892a6e1c94e31aa741e6ca3f5eccbd5`

```dockerfile
```

-	Layers:
	-	`sha256:eba2e214d28c53b66c8c0103ec367c10c2cfa56ac823ede9d4cb8d4e24f696bb`  
		Last Modified: Tue, 19 May 2026 23:19:28 GMT  
		Size: 20.0 KB (20024 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:latest` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:565d45453e64b33c462e36ec6732d21e4e0b94f62749115a22654b74494f11b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116314831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c28dd2d50e3a3fced5a9e6940587e12d801624fb557311c0d19af628006f9fe`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:22:21 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Tue, 19 May 2026 23:22:21 GMT
ARG VARNISH_VERSION_NUMBER=9.0.3-1
# Tue, 19 May 2026 23:22:21 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Tue, 19 May 2026 23:22:21 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Tue, 19 May 2026 23:22:21 GMT
ENV VARNISH_SIZE=100M
# Tue, 19 May 2026 23:22:21 GMT
ENV VSM_NOPID=1
# Tue, 19 May 2026 23:22:21 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.3-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Tue, 19 May 2026 23:22:21 GMT
WORKDIR /etc/varnish
# Tue, 19 May 2026 23:22:21 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:22:21 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Tue, 19 May 2026 23:22:21 GMT
COPY index.html /var/www/html/ # buildkit
# Tue, 19 May 2026 23:22:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Tue, 19 May 2026 23:22:21 GMT
USER varnish
# Tue, 19 May 2026 23:22:21 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Tue, 19 May 2026 23:22:21 GMT
CMD []
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533b40a52f530d1c340c9db810e6c109be13b6e42aa4080cf52a137ec4d5d63e`  
		Last Modified: Tue, 19 May 2026 23:22:35 GMT  
		Size: 86.2 MB (86170029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3092a0e13cad6d2721e6955698724fee5c700e1e3cf473d2a1ce5c34dc568705`  
		Last Modified: Tue, 19 May 2026 23:22:32 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db45bd38506479f67a657c2933fb9f67cd999cc16657d7ef96a979661843e31`  
		Last Modified: Tue, 19 May 2026 23:22:32 GMT  
		Size: 1.0 KB (1006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79793aa37d81effa317b9eb89168681b3d14ed12d75c28f68fdfbb1c1af9b72`  
		Last Modified: Tue, 19 May 2026 23:22:33 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:latest` - unknown; unknown

```console
$ docker pull varnish@sha256:1ea3079afb688b3feed66d3487ed379c3dd66e66c5f155855b91d4e26a93d619
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 KB (20152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d45063a85abed5cc64df993208e810ce2c3a0c144a7657ff42871b4712c02c6d`

```dockerfile
```

-	Layers:
	-	`sha256:3b1d1f0a1819fc3090e757e0391e9af859ac228fe8f9d5ca44a9c9767a78bebe`  
		Last Modified: Tue, 19 May 2026 23:22:32 GMT  
		Size: 20.2 KB (20152 bytes)  
		MIME: application/vnd.in-toto+json
