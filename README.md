Go-sync-evaluation
==================

A drop-in replacement package for "sync" to evaluate locks.

## Installation

	go get github.com/larspensjo/Go-sync-evaluation/evalsync

## Usage instructions

To use this package, simply replace the usual sync package as below.
Statistics will be collected for:
* RD del (Longest wait for a RLock)
* WR del (Longest wait for a Lock)
* RD op (slowest RLock/RUnlock period)
* WR op (slowest Lock/Unlock period)

There will also be information who was the reason for the delay.

`import sync "github.com/larspensjo/Go-sync-evaluation/evalsync"`

Return an array of strings with information   
`func Eval() []string`

Enable the measurements with the flag `-evalsync.v=1`. Using level 2, extra information
will be printed in the log.

## Copyright and licensing

Distributed under GNU General Public License.
