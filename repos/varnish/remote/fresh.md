## `varnish:fresh`

```console
$ docker pull varnish@sha256:91cd10d2aa08f293054a75db600b7093ee1b8a7e413b6c9435015c890575d6a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `varnish:fresh` - linux; amd64

```console
$ docker pull varnish@sha256:a633196ce5f4abc0746be632c7a30073fe191860b4881353c326f47f42381f1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.0 MB (123984303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edb10adaa2e06f0fdcd8c3579392ebc669af212d8a6d90a8b1a3f1aaec04dcf1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Fri, 10 Apr 2026 17:47:39 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Fri, 10 Apr 2026 17:47:39 GMT
ARG VARNISH_VERSION_NUMBER=9.0.1-1
# Fri, 10 Apr 2026 17:47:39 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Fri, 10 Apr 2026 17:47:39 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Fri, 10 Apr 2026 17:47:39 GMT
ENV VARNISH_SIZE=100M
# Fri, 10 Apr 2026 17:47:39 GMT
ENV VSM_NOPID=1
# Fri, 10 Apr 2026 17:47:39 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.1-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 10 Apr 2026 17:47:39 GMT
WORKDIR /etc/varnish
# Fri, 10 Apr 2026 17:47:39 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 17:47:39 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 10 Apr 2026 17:47:39 GMT
COPY index.html /var/www/html/ # buildkit
# Fri, 10 Apr 2026 17:47:39 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 10 Apr 2026 17:47:39 GMT
USER varnish
# Fri, 10 Apr 2026 17:47:39 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 10 Apr 2026 17:47:39 GMT
CMD []
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7edb459dc695b9ed55dc9d57d42fe814817dff184d4eaff0f36ef9301b9a508a`  
		Last Modified: Fri, 10 Apr 2026 17:47:55 GMT  
		Size: 94.2 MB (94205783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e81bb3cf144ca0a88f8fa0d1bfaa98e66c19c4d21cddc52ba6c9643a6a026aa`  
		Last Modified: Fri, 10 Apr 2026 17:47:52 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2abd877ddaceccbfa26d173d45cebe74a8ab9aedca64142400c31d05813662`  
		Last Modified: Fri, 10 Apr 2026 17:47:52 GMT  
		Size: 1.0 KB (1006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760a134477850f33d57d335e741110ad0633eb6ae64cd3edc62f8bb355518530`  
		Last Modified: Fri, 10 Apr 2026 17:47:52 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:8b5764c5ce75e8a002bbb573534efc73ad65880efa608d7d3fd8cc3dc4d786a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:364d0bdf5fe043ed4dfb0872e56f83e6be572c5e8a3bb2a9aee34b697d5a935a`

```dockerfile
```

-	Layers:
	-	`sha256:e2d648c6c09dcef4353d46af054a1b1d4b5528ecdd7967e9e3972c69ba6c2f16`  
		Last Modified: Fri, 10 Apr 2026 17:47:52 GMT  
		Size: 19.7 KB (19722 bytes)  
		MIME: application/vnd.in-toto+json

### `varnish:fresh` - linux; arm64 variant v8

```console
$ docker pull varnish@sha256:f9cd1a697def9d65f20a3a3334d47159cd2ad63aec6bce78d6d8f885adcc052b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.3 MB (118349593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1ac8463ddfbad01e0651f120580f18d99b3fb4c7ec04a88e01b5c921b4e3aef`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Fri, 10 Apr 2026 17:11:33 GMT
ARG REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344
# Fri, 10 Apr 2026 17:11:33 GMT
ARG VARNISH_VERSION_NUMBER=9.0.1-1
# Fri, 10 Apr 2026 17:11:33 GMT
ARG TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
# Fri, 10 Apr 2026 17:11:33 GMT
ENV VMOD_DEPS=autoconf-archive automake curl libtool make pkg-config python3-sphinx varnish-dev
# Fri, 10 Apr 2026 17:11:33 GMT
ENV VARNISH_SIZE=100M
# Fri, 10 Apr 2026 17:11:33 GMT
ENV VSM_NOPID=1
# Fri, 10 Apr 2026 17:11:33 GMT
# ARGS: REPO_FINGERPRINT=694566269779DFAC975ED9BDD0525EAE838B3344 VARNISH_VERSION_NUMBER=9.0.1-1 TOOLBOX_COMMIT=da1c5ce23d2ad81032bb45627d10a8dcb2c6f1d9
RUN set -ex;     . /etc/os-release;     VARNISH_VERSION=$VARNISH_VERSION_NUMBER~$VERSION_CODENAME;     BASE_PKGS="apt-utils automake git gpg libgetdns-dev libtool make pkg-config python3-docutils";     export DEBIAN_FRONTEND=noninteractive;     export DEBCONF_NONINTERACTIVE_SEEN=true;         apt-get update;     apt-get install -y curl $BASE_PKGS;     mkdir -p /etc/apt/keyrings;     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys $REPO_FINGERPRINT;     gpg --batch --armor --export "$REPO_FINGERPRINT" > /etc/apt/keyrings/varnish.gpg;     echo "deb [signed-by=/etc/apt/keyrings/varnish.gpg] https://packages.varnish-software.com/varnish/$ID $VERSION_CODENAME main" | tee -a /etc/apt/sources.list.d/varnish.list;     apt-get update;     adduser --uid 1000 --quiet --system --no-create-home --home /nonexistent --group varnish;     adduser --uid 1001 --quiet --system --no-create-home --home /nonexistent --ingroup varnish vcache;     adduser --uid 1002 --quiet --system --no-create-home --home /nonexistent --ingroup varnish varnishlog;         apt-get update;     apt-get install -y --no-install-recommends 				varnish=${VARNISH_VERSION} 				varnish-dev=${VARNISH_VERSION} 				varnish-modules=${VARNISH_VERSION} 				vmod-cfg=${VARNISH_VERSION} 				vmod-digest=${VARNISH_VERSION} 				vmod-fileserver=${VARNISH_VERSION} 				vmod-geoip2=${VARNISH_VERSION} 				vmod-jq=${VARNISH_VERSION} 				vmod-querystring=${VARNISH_VERSION} 				vmod-redis=${VARNISH_VERSION} 				vmod-reqwest=${VARNISH_VERSION} 				vmod-rers=${VARNISH_VERSION} 				vmod-uuid=${VARNISH_VERSION};         git clone https://github.com/varnish/toolbox.git;     cd toolbox;     git checkout $TOOLBOX_COMMIT;     cp install-vmod/install-vmod /usr/local/bin/;     cp vcls/verbose_builtin/verbose_builtin.vcl vcls/hit-miss/hit-miss.vcl /etc/varnish/;         apt-mark hold varnish;     apt-get -y purge --auto-remove $BASE_PKGS varnish-dev;     rm -rf /var/lib/apt/lists/* /usr/lib/varnish/vmods/libvmod_*.la;     rm -rf ~/.gnupg;     chown varnish /var/lib/varnish;     mkdir -p -m 1777 /var/lib/varnish/varnishd # buildkit
# Fri, 10 Apr 2026 17:11:33 GMT
WORKDIR /etc/varnish
# Fri, 10 Apr 2026 17:11:33 GMT
COPY scripts/ /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 17:11:33 GMT
COPY default.vcl /etc/varnish/ # buildkit
# Fri, 10 Apr 2026 17:11:33 GMT
COPY index.html /var/www/html/ # buildkit
# Fri, 10 Apr 2026 17:11:33 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Fri, 10 Apr 2026 17:11:33 GMT
USER varnish
# Fri, 10 Apr 2026 17:11:33 GMT
EXPOSE map[80/tcp:{} 8443/tcp:{}]
# Fri, 10 Apr 2026 17:11:33 GMT
CMD []
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e3af3bca1472f9f298828fce4d29fa27c20acaf5822194ff32e4125fe8fcb31`  
		Last Modified: Fri, 10 Apr 2026 17:11:47 GMT  
		Size: 88.2 MB (88208151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89383f887ad181889cb93db922142949358a7dc9965d5ee382ed751fb78dd39`  
		Last Modified: Fri, 10 Apr 2026 17:11:44 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e00dc83ad7bf1fff59acff685454469c3130a9106f07f4afa39272b96eb7ae5`  
		Last Modified: Fri, 10 Apr 2026 17:11:44 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16bd7a322abd7119444c3a9289524ffe41f6570522ecdb1f02510688b36391f2`  
		Last Modified: Fri, 10 Apr 2026 17:11:44 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `varnish:fresh` - unknown; unknown

```console
$ docker pull varnish@sha256:d96ae547aadc8aa0e2f5194b5dad6311f9eaadfb2681b4891d37c204b70f1c25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac038aa58b7c7e03b15a8363daa3c33cab1d8d6a63740d5bb691edf8e68245c5`

```dockerfile
```

-	Layers:
	-	`sha256:608227b037937cd986038e26304d6c5f4326b3fd14b8e1846cae3118b3db6278`  
		Last Modified: Fri, 10 Apr 2026 17:11:44 GMT  
		Size: 19.8 KB (19838 bytes)  
		MIME: application/vnd.in-toto+json
