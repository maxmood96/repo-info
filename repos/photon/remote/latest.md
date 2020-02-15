## `photon:latest`

```console
$ docker pull photon@sha256:9f109dea78d3e6ffbf6c37c35c6068a58c915687dd64a3995b88a161711fb913
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `photon:latest` - linux; amd64

```console
$ docker pull photon@sha256:9a1a38e42b35e339791d64834323574a81b8a66b19ac06e69837120b5c3750eb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15150939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6e84a333eca98650afe6e41578464a0b50c9673d848fb730520b932bb3b6ced`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Feb 2020 01:30:46 GMT
ADD file:199618049d5a46954d929aaa712be1fd6f51dab56e562888cbe82b65d9dcc3c6 in / 
# Sat, 15 Feb 2020 01:30:46 GMT
LABEL name=Photon OS x86_64/3.0 Base Image vendor=VMware build-date=20200214
# Sat, 15 Feb 2020 01:30:46 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2fc2bf5a53620851213630f1381dafe2ae9c99e0fee4853e935cce82bf0bfc0b`  
		Last Modified: Sat, 15 Feb 2020 01:31:33 GMT  
		Size: 15.2 MB (15150939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `photon:latest` - linux; arm64 variant v8

```console
$ docker pull photon@sha256:7397246049d858edb71f73cf8f2fb851775812ea5e11dde65f972ede2a11ef04
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (12958897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df71ae253426363c63bb1188af576393b8a9d14b0a8e08d86f572a3736c03c1e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Feb 2020 01:55:39 GMT
ADD file:e6ad3cee3c673f70dd1271684ee9c8d19100a9b8d81948b9eafd7e91f4b266ec in / 
# Sat, 15 Feb 2020 01:55:47 GMT
LABEL name=Photon OS aarch64/3.0 Base Image vendor=VMware build-date=20200214
# Sat, 15 Feb 2020 01:55:48 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2471f14aa92a05fa0e95245b1cc2c95e6f0d3c92b3c6a2cd1e92550d96ff83ef`  
		Last Modified: Sat, 15 Feb 2020 01:56:07 GMT  
		Size: 13.0 MB (12958897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
