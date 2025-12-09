## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:d7dc8169de3d55fdaa6cbfc715365f7c1310e6284b779a15cfc43de82d3845a3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:a957753045a14203151774d16129aaefdb44e9de960fe4ea3862b1fd04bd3f20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59672916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5cec34e2b0e6bca6155929d2e85b7d83341aaf1e1c3b350957c9d32dbb6a754`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:13:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:13:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:13:33 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 08 Dec 2025 23:13:36 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:13:36 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:2981f7e8980b9f4b6605026e1c5f99b4971ebba15f626e46904554de09f324f4`  
		Last Modified: Mon, 08 Dec 2025 22:17:46 GMT  
		Size: 49.3 MB (49289520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86871226ba9e77e017a7f2b7e85647edf6c1322698a2147ee1f40c433f87262a`  
		Last Modified: Mon, 08 Dec 2025 23:13:52 GMT  
		Size: 10.3 MB (10289817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7768d5018bc2656c9391afd8cee18c2959cf5475de87e640b86d192f56789ff4`  
		Last Modified: Mon, 08 Dec 2025 23:13:51 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272bd37d8a9122e74d6ebc239b01712048af64cb75e5d1afc4de86f245a72ae3`  
		Last Modified: Mon, 08 Dec 2025 23:13:51 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac388fb72582b7db61d9b521c71d9e2b66d16efa9cc727c31c59d5db86994a3b`  
		Last Modified: Mon, 08 Dec 2025 23:13:51 GMT  
		Size: 90.2 KB (90231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dda49dee40fb2520bf9a3cf6fe856b91f8df4e1560100da7ad562d269f37195`  
		Last Modified: Mon, 08 Dec 2025 23:13:51 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:78e64490e81120e801b89a4fd6ef3114c94f8ce4c011d4c1291a42ae081d977d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6b343a0d90c41efd03a5dd3c8dbff1a9020ccd382a482e0856f54b5b6dd648e`

```dockerfile
```

-	Layers:
	-	`sha256:8cd14e3eda9f174f3a690c3e2674319aea491ed475f25ef8d571b96dc0194512`  
		Last Modified: Tue, 09 Dec 2025 02:09:01 GMT  
		Size: 3.6 MB (3613069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf8a352263cee4798d3401d54f82423d9b7b04fc3a8d0c748e98f555ca3c6340`  
		Last Modified: Tue, 09 Dec 2025 02:09:02 GMT  
		Size: 16.3 KB (16282 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:cbe051ff9e65e938ef970ed213bed1845e12d099468e69ee359adf3f29216d54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59817985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29d723f4d19be58aaf30cbc45c642741452d891db5e4ce1244af5c7ab9483bd6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:53:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:53:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:53:59 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 03:54:03 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:54:03 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:9276e76e62afd8421516059c0238d0d2bba58227af1cbce32b43d67781151ea2`  
		Last Modified: Tue, 18 Nov 2025 01:14:17 GMT  
		Size: 49.7 MB (49650232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a505c9bb250d77e4640e96c444c4fac586fc1433c373bbef83a7256e04d6ade`  
		Last Modified: Tue, 18 Nov 2025 03:54:19 GMT  
		Size: 10.1 MB (10073459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904db87cf72b19c511cfe31ac93b95a3ed1ba1f7c9bb7582ee6eb938d2e164d4`  
		Last Modified: Tue, 18 Nov 2025 03:54:17 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842dfa2696e5c96bc037b37dd0932b97434244d91043450150d9e96bdd37472b`  
		Last Modified: Tue, 18 Nov 2025 03:54:17 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaca400b700bdb23c02eff76b5d0d5caf6a698ebaf8497f19a82b8f417b1b01e`  
		Last Modified: Tue, 18 Nov 2025 03:54:17 GMT  
		Size: 90.9 KB (90944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d36449c0d721c1d3cd641f286b2d678c32dcaa57534317626ed05a07c2d19fe`  
		Last Modified: Tue, 18 Nov 2025 03:54:17 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6e09f67ac5afd71c56c4130e2c079060e9181289a300b5159f7fdcc66744b050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3631030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72700cb5e900ded97e722e6c8b510c0b93dc64d74713213f9746adc344fea7d`

```dockerfile
```

-	Layers:
	-	`sha256:9c9cb02fac134943ac6de2142d5414212aaa7d7329798636b6a8f64c46838920`  
		Last Modified: Tue, 18 Nov 2025 05:10:07 GMT  
		Size: 3.6 MB (3614596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52009749de1793d97606f0008b38292d4695967e6cac6f459d6a77f967bde8c8`  
		Last Modified: Tue, 18 Nov 2025 05:10:08 GMT  
		Size: 16.4 KB (16434 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:b187bea3f10f39ea07ee4101dc0a3f18abbe7be34d2cff2bd6f7b49e13f3155b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61358559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dafef6df1ba7f540161567b41abc65dc5bdb8501cc5fbcddaf3cacc06c4bdaf2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:15:35 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:15:36 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:15:36 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 08 Dec 2025 23:15:40 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:15:40 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:a63ab7a4f8b10d53e108dbe1e04ab9e369b75bfa91be99da84bbdfb688a906bc`  
		Last Modified: Mon, 08 Dec 2025 22:16:00 GMT  
		Size: 50.8 MB (50801649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd4b33922c04dbc376b8a5e1f0f1e92e63bb89043733e9f1faa4310e1504bd7f`  
		Last Modified: Mon, 08 Dec 2025 23:15:56 GMT  
		Size: 10.5 MB (10462938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288115e75d815edb522e43eef503792b7e9e6c88509ee7e9ba4a8f7072e4f953`  
		Last Modified: Mon, 08 Dec 2025 23:15:54 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641aa24ee325190ed8096c6c9438150c637d751260dc4f24335265186be298f3`  
		Last Modified: Mon, 08 Dec 2025 23:15:54 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c30ad08df9b38bd944f88c550208c2de69c4c644bcc8a39159b8149bbcab36a`  
		Last Modified: Mon, 08 Dec 2025 23:15:54 GMT  
		Size: 90.6 KB (90624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e48e15f7f8648267c2768f3207e320a23c1769e635224feb1f62bd2181b3e786`  
		Last Modified: Mon, 08 Dec 2025 23:15:54 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b7406b4bee75ddf498b716c53bb3d974de73215e6a867b443f199125346ea588
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d84d6396779efcbbaa4d5ca3717a85cea53fa601f8499d1d5e4932ecd0830673`

```dockerfile
```

-	Layers:
	-	`sha256:9689b9651a4bdf918275574dedc207d7f9b6a4d8deb9f363c0f94ac3816b45e0`  
		Last Modified: Tue, 09 Dec 2025 02:09:11 GMT  
		Size: 3.6 MB (3611018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:134c12f5888db88b0afd397425b7c86d8d384dd6dcfee36c93eb7abe2abb0f15`  
		Last Modified: Tue, 09 Dec 2025 02:09:12 GMT  
		Size: 16.2 KB (16247 bytes)  
		MIME: application/vnd.in-toto+json
