# SPDX-License-Identifier: BSD-3-Clause
# Copyright(c) 2017 Intel Corporation

# meson file, for building this example as part of a main DPDK build.
#
# To build this example as a standalone application with an already-installed
# DPDK instance, use 'make'

#rte_eth_read_clock is experimental
project('dpdk-daemon', 'c')

allow_experimental_apis = true

dpdk = dependency('libdpdk', required: true)
sqlite = dependency('sqlite3', required: true)

sources = files('main.c')

executable('dpdk-rxtx_callbacks', 
    sources: sources,
    dependencies: [dpdk,sqlite],
    install: true)
