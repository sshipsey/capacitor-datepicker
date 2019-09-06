# Capacitor DatePicker

[![npm](https://img.shields.io/npm/v/capacitor-datepicker.svg)](https://www.npmjs.com/package/capacitor-datepicker)
[![npm](https://img.shields.io/npm/dt/capacitor-datepicker.svg?label=npm%20downloads)](https://www.npmjs.com/package/capacitor-datepicker)
[![Build Status](https://travis-ci.org/triniwiz/capacitor-datepicker.svg?branch=master)](https://travis-ci.org/triniwiz/capacitor-datepicker)

## Installation

`npm i capacitor-datepicker`

## Usage

### TypeScript

```typescript
import { DatePicker } from 'capacitor-datepicker';

const picker = new DatePicker();
const current = new Date();
const response = await picker.show({
  mode: 'date',
  date: current.toISOString(), //  ISO 8601 datetime format
  theme: 'AppDialogTheme', // Android theme name uses 'DialogTheme' as the default,
  title: 'Choose a date',
  okText: 'Ok',
  cancelText: 'Cancel',
  okButtonColor: 'green',
  cancelButtonColor: 'red',
  titleTextColor: 'black', // IOS only
  titleBgColor: 'green', // IOS only
  is24Hours: false // available for time mode
});
const date = response.value;
```

## Api

| Method                           | Default | Type                         | Description |
| -------------------------------- | ------- | ---------------------------- | ----------- |
| show(options: DatePickerOptions) |         | `Promise<{ value: string }>` |             |
